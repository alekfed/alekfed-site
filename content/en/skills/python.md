+++
title = "Python"
subtitle = "Experience: 6 years"
tags = ['Languages']
date = 2020-03-24

# For description meta tag
description = "Something completely different."

# Comment next line and the default banner wil be used.
banner = 'img/python_v2.svg'

+++

For me, Python is a natural choice in cases when the problem in question doesn't have strict performance requirements or if there is some well-established library in Python ecosystem that can be used the problem.

# Web Frameworks

Of all the Python web frameworks variety, I worked with three:

- [FastAPI](https://fastapi.tiangolo.com/) was used to develop microservices for e-commerce platform that provides integration with Ozon, Wilberries, Tmall, Yandex.Market and Goods marketplaces. FastAPI is really pretty: native [typing](https://docs.python.org/3/library/typing.html) is used in the name of runtime validation ([pydantic](https://pydantic-docs.helpmanual.io/)), confident usage of `asyncio` capabilities, integration with `pytest`, and active advocacy of Dependency Injection which allows avoiding many problems with context passing. It's my primary choice for Python web services at the moment.

- [Django](https://www.djangoproject.com/) was used extensively for development of a monolithic application with various marketplace tools and configuration interfaces for testing equipment. Django is great for making “all-inclusive” standalone applications, but my microservices using it weren't very “micro”. Of course, [REST Framework](https://www.django-rest-framework.org/) is our everything!😄 It's a pity that Django doesn't seem to have a stable [asynchronous ORM](https://docs.djangoproject.com/en/3.1/topics/async/#async-safety), although the author of SQLAlchemy reasonably noted that sometimes asynchronous interaction [can be quite painful](https://techspot.zzzeek.org/2015/02/15/asynchronous-python-and-databases/).

- [Flask](https://flask.palletsprojects.com/en/1.1.x/) was used in the development of a back-end for the diagnostics system (React was used for front-end, see [JavaScript](/skills/js)). Because I later discovered FastAPI, I've never used Flask again, and  I remember only a couple of things about it: for each sneeze you need to install some special plugin ([SQLAlchemy](https://flask-sqlalchemy.palletsprojects.com/en/ 2.x /), [HTTPAuth](https://flask-httpauth.readthedocs.io/en/latest/index.html) ...) and that all applications are divided into [Blueprints](https: // flask.palletsprojects.com/en/1.1.x/blueprints/).

# ORM and Databases

In Python I usually work with databases using ORM ([SQLAlchemy](https://docs.sqlalchemy.org/en/14/orm/) or [Django](https://docs.djangoproject.com/en/3.1/topics/db/queries/)), although sometimes [SQLAlchemy Core](https://docs.sqlalchemy.org/en/14/core/) can be enough. Raw SQL queries are certainly indispensable for optimizing performance in the face of growing service loads, however, if the service is really experiencing these kinds of problems, perhaps it's time to rethink the choice of Python as the service implementation language?..

Before the release of [SQLAlchemy 1.4](https://www.sqlalchemy.org/blog/2021/03/15/sqlalchemy-1.4.0-released/), which officially added support for `asyncio` via` asyncpg` and ` aiomysql`, it was also interesting to experiment with libraries that benefit from `asyncio`, like [Tortoise](https://tortoise-orm.readthedocs.io/en/latest/), [GINO](https://python-gino.org/) or [databases](https://www.encode.io/databases/). They're not so relevant now, though.

# GraphQL

This piece of Facebook's engineering art gained considerable popularity over the last few years, so I couldn't stand aside, especially in the light of solving the perennial problem of back-end/front-end interfaces coordination.

Despite the obvious dominance of JavaScript in this area, there are some good GraphQL-libraries in the Python ecosystem as well:

- [Graphene](https://graphene-python.org/) is one of the first libraries and apparently the most popular. After using it for a while, I came to the conclusion that an additional layer between GraphQL schemas and a DB layer is not a very good idea. Starlette previously had built-in support for Graphene, but [it's been removed](https://github.com/encode/starlette/pull/1135).

- [Ariadne](https://ariadnegraphql.org/) is younger than Graphene, but it fixes its main drawback: schemas aren't written using special classes but are parsed directly from files with GraphQL schemas. I used Ariadne with [Starlette](https://ariadnegraphql.org/docs/starlette-integration), it worked fine (except for `DataLoader`, which is discussed below).

- [Strawberry](https://strawberry.rocks/) is a very recent addition based on [Python's answer to structs](https://docs.python.org/3/library/dataclasses.html). Couple of months ago there were stubs all over its documentation, so I didn't use it much. It will be very interesting to try when this 🍓 ripens.

The biggest problem with all these libraries was the lack of some mechanism that caches DB queries and automatically compiles them into a batch query. ([DataLoader](https://github.com/graphql/dataloader)). To some extent, this idea was implemented for both Ariadne and Graphene (perhaps, Raspberry [can handle it](https://strawberry.rocks/docs/features/dataloaders) finally?), but conjugation of these solutions with queries to databases is still not a very pleasant experience, especially in the face of constantly changing GraphQL schemas.

# Code Quality

I try to use [typing](https://docs.python.org/3/library/typing.html) all the time and to control types with static analyzers like [mypy](https://github.com/python/mypy) and [Pyright](https://github.com/microsoft/pyright) (by the way, the latter is very good as [LSP server](https://github.com/emacs-lsp/lsp-pyright) - more snappier than [palantir's](https://github.com/palantir/python-language-server) one for sure).

Of the linters, I mostly use [flake8](https://flake8.pycqa.org/en/latest/), but I dropped using [pylint](https://www.pylint.org/) at some point. [Black](https://github.com/psf/black) and [yapf](https://github.com/google/yapf) didn't found much support in my past teams, so I'm not used to using them.

And, since, in my opinion, tests are a mandatory element of CI, [pytest](https://docs.pytest.org/en/stable/) is my man!😄 (by the way, [qutebrowser](https://qutebrowser.org /) by the same guy is 🔥 as well)

# (Data) Science & Machine Learning

Python ecosystem has a lot of excellent scientific libraries which had come in handy while I did some research works in graduate school. I often used [pandas](https://pandas.pydata.org/) to analyze devices that I developed (later, it also turned out that `pandas` does quite well with Keras, which I used to experiment with UAV control systems).

Since I had a traditional control systems engineering training at university, naturally, MATLAB was my first language for control system development. However, at some point I noticed how well everything works out with `pandas` and decided to switch to Python for control systems as well. The [python-control](https://python-control.readthedocs.io/en/0.9.0/) library covered my needs quite well.

Later, while working on UAV control systems, I had the idea to make an adaptive controller based on Reinforcement Learning, so I started to fiddle with [Keras](https://keras.io/). Unfortunately, it turned out that neural networks isn't very suitable technology for such a task (for more details, see the [control systems](/skills/math_control)).

Other ML work was done while working on an e-commerce platform. This time it was decided to use [Pytorch](https://pytorch.org/) because, despite its enourmous size, [torchvision](https://pytorch.org/vision/0.8/index.html) fit well to the task at hand, and the presence of the necessary [pre-trained models](https://github.com/Cadene/pretrained-models.pytorch#installation) was clearly a plus. The result was positive, but project was frozen at some point.

___
# Illustration

I didn't expect a kind of spanish inquisition!

It took me longer to create this illustration than everything else! (not taken together though) Initially, I wanted to create some kind of a collage in the spirit of Terry Gilliam's applicative animations with references to the incomparable [Holy Grail](https://en.wikipedia.org/wiki/Monty_Python_and_the_Holy_Grail) and [The Life of Brian]( https://en.wikipedia.org/wiki/Monty_Python's_Life_of_Brian) and a bunch of libraries that I happened to use:

![Python version 1](/img/python.png)

But I didn't like the result. More precisely, I didn't like how it looked in the general context. So, in the end, I decided that I need [something completely different](https://en.wikipedia.org/wiki/And_Now_for_Something_Completely_Different)!😅
