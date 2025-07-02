
⚠️  Limitations
===============


* Provider missing support incomplete implementation: link to the issue with all incomplete implementations of Snowflake entities in the provider

  * For such entities one has to use ``snowflake_execute`` resource or snowsql provider for multiline queries
  * TODO: examples

* Partial application of changes

  * TODO contrast with SnowDDL https://docs.snowddl.com/guides/other-guides/limitations-and-workarounds#partial-application-of-config
  * we rely on terraform mechanism to deal with partially applied changes. rerunning the plan and apply step any number of times works as a debugging pipeline
  * It is important to always explicitly use the ``depends_on`` argument in terraform resources in order to prevent unnecessary issues during apply step.

* https://docs.snowddl.com/guides/other-guides/limitations-and-workarounds#renaming-of-objects

  * TODO research and write but generally we can use terraform move for renaming objects

* Lower case identifiers are supported and handled like in Snowflake, but we do recommend avoiding that






.. toctree::
   :maxdepth: 2
   :caption: Contents:

