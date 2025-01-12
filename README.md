<!-- Generated with Stardoc: http://skydoc.bazel.build -->

# Bazel rules for extracting metadata about HTTP APIs from `proto_library` rules.

## `MODULE.bazel`

```
bazel_dep(
    name = "com_github_bcsgh_proto_api",
    version = ...,
)
```

<a id="gen_proto_api"></a>

## gen_proto_api

<pre>
load("@com_github_bcsgh_proto_api//proto_api:proto_api.bzl", "gen_proto_api")

gen_proto_api(<a href="#gen_proto_api-name">name</a>, <a href="#gen_proto_api-h">h</a>, <a href="#gen_proto_api-h_namespace">h_namespace</a>, <a href="#gen_proto_api-include_guard">include_guard</a>, <a href="#gen_proto_api-js">js</a>, <a href="#gen_proto_api-js_module">js_module</a>, <a href="#gen_proto_api-proto">proto</a>, <a href="#gen_proto_api-type">type</a>)
</pre>

Generate JS and C++ code that exposes the same string constants.

**ATTRIBUTES**


| Name  | Description | Type | Mandatory | Default |
| :------------- | :------------- | :------------- | :------------- | :------------- |
| <a id="gen_proto_api-name"></a>name |  A unique name for this target.   | <a href="https://bazel.build/concepts/labels#target-names">Name</a> | required |  |
| <a id="gen_proto_api-h"></a>h |  The generated C++ header file.   | <a href="https://bazel.build/concepts/labels">Label</a> | optional |  `None`  |
| <a id="gen_proto_api-h_namespace"></a>h_namespace |  Override the namespace to use in the C++ header file.   | String | optional |  `""`  |
| <a id="gen_proto_api-include_guard"></a>include_guard |  Override the include-guard to use in the C++ header file.   | String | optional |  `""`  |
| <a id="gen_proto_api-js"></a>js |  The generated JavaScript file.   | <a href="https://bazel.build/concepts/labels">Label</a> | optional |  `None`  |
| <a id="gen_proto_api-js_module"></a>js_module |  Override the goog.module to use in the JS file.   | String | optional |  `""`  |
| <a id="gen_proto_api-proto"></a>proto |  A proto_pimrary rule to generate from.   | <a href="https://bazel.build/concepts/labels">Label</a> | required |  |
| <a id="gen_proto_api-type"></a>type |  The type of output to use   | String | optional |  `"goog"`  |


## Setup (for development)
To configure the git hooks, run `./.git_hooks/setup.sh`
