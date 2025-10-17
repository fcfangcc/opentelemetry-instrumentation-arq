OpenTelemetry Arq Instrumentation
===================================================

This library provides automatic and manual instrumentation of `arq <https://github.com/python-arq/arq>`_

auto-instrumentation using the opentelemetry-instrumentation package is also supported.


Installation
------------

.. code-block:: shell

    pip install opentelemetry-instrumentation-arq

Usage
------

.. code-block:: python

    from opentelemetry.instrumentation.arq import ArqInstrumentor

    ArqInstrumentor.instrument()

Warning
---------
Because of the protocol problem of arq , if the client side adds OTEL,  the server side will report an error if server does not add OTEL.

server side adds OTEL and client not add OTEL is no problem.

Test
------

.. code-block:: shell

    python -m unittest tests/*


References
----------

* `OpenTelemetry Project <https://opentelemetry.io/>`_
* `OpenTelemetry Python Examples <https://github.com/open-telemetry/opentelemetry-python/tree/main/docs/examples>`_
