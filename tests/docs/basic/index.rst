Welcome to test's documentation!
================================

.. jinja::

   .. include:: ../../../README.rst

after include

.. jinja:: first_ctx

    {% for k, v in topics.items() %}

    {{k}}
    ~~~~~
    {{v}}
    {% endfor %}

after first context

.. jinja:: second_ctx
   :file: tests/docs/basic/jinja_template.jinja
   :header_char: ~

after second context

.. jinja:: fourth_ctx fourth_ctx_key
    :debug:

    Lists
    -----

    {% for o in objects -%}
        {%- if o is instanceof list -%}
            {%- for x in o -%}
                - {{ x|bold }}
            {% endfor -%}
        {%- endif -%}
    {%- endfor %}

after third context

first context with debug on

.. jinja:: first_ctx
    :debug:

    {% for k, v in topics.items() %}

    {{k}}
    ~~~~~
    {{v}}
    {% endfor %}

second context with debug on

.. jinja:: second_ctx
   :file: tests/docs/basic/jinja_template.jinja
   :header_char: ~
   :debug:
