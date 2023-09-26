Pyramid
=======

.. image:: https://github.com/Pylons/Pyramid/workflows/Build%20and%20test/badge.svg?branch=main
        :target: https://github.com/Pylons/Pyramid/actions?query=workflow%3A%22Build+and+test%22
        :alt: main CI Status

.. image:: https://readthedocs.org/projects/pyramid/badge/?version=main
        :target: https://docs.pylonsproject.org/projects/pyramid/en/main
        :alt: main Documentation Status

.. image:: https://img.shields.io/badge/IRC-Libera.Chat-blue.svg
        :target: https://web.libera.chat/#pyramid
        :alt: IRC Libera.Chat

Pyramidは小さく、高速で、地に足の着いた、オープンソースのPythonウェブフレームワークです。
これにより、実世界のウェブアプリケーションの開発とデプロイメントがより楽しく、予測可能で、生産的になります。
Pyramidを試してみて、そのアドオンやドキュメンテーションを閲覧し、概要を把握してください。
`Try Pyramid <https://trypyramid.com/>`_, browse its add-ons and documentation, and get an overview.

.. code-block:: python

    from wsgiref.simple_server import make_server
    from pyramid.config import Configurator
    from pyramid.response import Response

    def hello_world(request):
        return Response('Hello World!')

    if __name__ == '__main__':
        with Configurator() as config:
            config.add_route('hello', '/')
            config.add_view(hello_world, route_name='hello')
            app = config.make_wsgi_app()
        server = make_server('0.0.0.0', 6543, app)
        server.serve_forever()

Pyramid is a project of the `Pylons Project <https://pylonsproject.org>`_.

Support and Documentation
-------------------------

See `Pyramid Support and Development
<https://docs.pylonsproject.org/projects/pyramid/en/latest/#support-and-development>`_
for documentation, reporting bugs, and getting support.

Developing and Contributing
---------------------------

See `HACKING.txt <https://github.com/Pylons/pyramid/blob/main/HACKING.txt>`_ and
`contributing.md <https://github.com/Pylons/pyramid/blob/main/contributing.md>`_
for guidelines on running tests, adding features, coding style, and updating
documentation when developing in or contributing to Pyramid.

License
-------

Pyramid is offered under the BSD-derived `Repoze Public License
<http://repoze.org/license.html>`_.

Authors
-------

Pyramid is made available by `Agendaless Consulting <https://agendaless.com>`_
and a team of `contributors
<https://github.com/Pylons/pyramid/graphs/contributors>`_.
