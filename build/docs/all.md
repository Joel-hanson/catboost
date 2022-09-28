*Do not edit, this file is generated from comments to macros definitions using `ya dump conf-docs --dump-all`.*

# ya.make and core.conf commands

General info: [How to write ya.make files](https://wiki.yandex-team.ru/yatool/HowToWriteYaMakeFiles)

## Table of contents

   * [Multimodules](#multimodules)
       - Multimodule [DLL_JAVA](#multimodule_DLL_JAVA)
       - Multimodule [DOCS](#multimodule_DOCS)
       - Multimodule [DYNAMIC_LIBRARY](#multimodule_DYNAMIC_LIBRARY)
       - Multimodule [FBS_LIBRARY](#multimodule_FBS_LIBRARY)
       - Multimodule [JAR_PROGRAM](#multimodule_JAR_PROGRAM)
       - Multimodule [JAVA_CONTRIB_PROGRAM](#multimodule_JAVA_CONTRIB_PROGRAM)
       - Multimodule [JAVA_PROGRAM](#multimodule_JAVA_PROGRAM)
       - Multimodule [JTEST](#multimodule_JTEST)
       - Multimodule [JTEST_FOR](#multimodule_JTEST_FOR)
       - Multimodule [JTEST_YMAKE](#multimodule_JTEST_YMAKE)
       - Multimodule [JUNIT5](#multimodule_JUNIT5)
       - Multimodule [JUNIT5_YMAKE](#multimodule_JUNIT5_YMAKE)
       - Multimodule [MAPS_IDL_LIBRARY](#multimodule_MAPS_IDL_LIBRARY)
       - Multimodule [MKDOCS](#multimodule_MKDOCS)
       - Multimodule [PROTO_LIBRARY](#multimodule_PROTO_LIBRARY)
       - Multimodule [PY23_LIBRARY](#multimodule_PY23_LIBRARY)
       - Multimodule [PY23_NATIVE_LIBRARY](#multimodule_PY23_NATIVE_LIBRARY)
       - Multimodule [PY23_TEST](#multimodule_PY23_TEST)
       - Multimodule [PY3TEST](#multimodule_PY3TEST)
       - Multimodule [PY3_PROGRAM](#multimodule_PY3_PROGRAM)
       - Multimodule [SANDBOX_PY23_TASK](#multimodule_SANDBOX_PY23_TASK)
       - Multimodule [SANDBOX_PY3_TASK](#multimodule_SANDBOX_PY3_TASK)
       - Multimodule [SANDBOX_TASK](#multimodule_SANDBOX_TASK)
       - Multimodule [SSQLS_LIBRARY](#multimodule_SSQLS_LIBRARY)
       - Multimodule [YQL_UDF](#multimodule_YQL_UDF)
   * [Modules](#modules)
       - Module [AAR](#module_AAR)
       - Module [AAR_PROXY_LIBRARY](#module_AAR_PROXY_LIBRARY)
       - Module [ASRC_LIBRARY](#module_ASRC_LIBRARY)
       - Module [BOOSTTEST](#module_BOOSTTEST)
       - Module [BOOSTTEST_WITH_MAIN](#module_BOOSTTEST_WITH_MAIN)
       - Module [CI_GROUP](#module_CI_GROUP)
       - Module [CONTAINER](#module_CONTAINER)
       - Module [CONTAINER_LAYER](#module_CONTAINER_LAYER)
       - Module [CPP_STYLE_TEST](#module_CPP_STYLE_TEST)
       - Module [CUSTOM_BUILD_LIBRARY](#module_CUSTOM_BUILD_LIBRARY)
       - Module [DEFAULT_IOS_INTERFACE](#module_DEFAULT_IOS_INTERFACE)
       - Module [DEV_DLL_PROXY](#module_DEV_DLL_PROXY)
       - Module [DLL](#module_DLL)
       - Module [DLL_PROXY](#module_DLL_PROXY)
       - Module [DLL_PROXY_LIBRARY](#module_DLL_PROXY_LIBRARY)
       - Module [DLL_TOOL](#module_DLL_TOOL)
       - Module [DLL_UNIT](#module_DLL_UNIT)
       - Module [DOCS_LIBRARY](#module_DOCS_LIBRARY)
       - Module [EXECTEST](#module_EXECTEST)
       - Module [EXTERNAL_JAVA_LIBRARY](#module_EXTERNAL_JAVA_LIBRARY)
       - Module [FAT_OBJECT](#module_FAT_OBJECT)
       - Module [FUZZ](#module_FUZZ)
       - Module [GO_DLL](#module_GO_DLL)
       - Module [GO_LIBRARY](#module_GO_LIBRARY)
       - Module [GO_PROGRAM](#module_GO_PROGRAM)
       - Module [GO_TEST](#module_GO_TEST)
       - Module [GTEST](#module_GTEST)
       - Module [GTEST_UGLY](#module_GTEST_UGLY)
       - Module [G_BENCHMARK](#module_G_BENCHMARK)
       - Module [IOS_INTERFACE](#module_IOS_INTERFACE)
       - Module [JAR_LIBRARY](#module_JAR_LIBRARY)
       - Module [JAVA_CONTRIB](#module_JAVA_CONTRIB)
       - Module [JAVA_CONTRIB_PROXY](#module_JAVA_CONTRIB_PROXY)
       - Module [JAVA_LIBRARY](#module_JAVA_LIBRARY)
       - Module [JSRC_LIBRARY](#module_JSRC_LIBRARY)
       - Module [JSRC_PROXY_MOBILE_LIBRARY](#module_JSRC_PROXY_MOBILE_LIBRARY)
       - Module [LIBRARY](#module_LIBRARY)
       - Module [MCU_PROGRAM](#module_MCU_PROGRAM)
       - Module [MOBILE_BOOST_TEST_APK](#module_MOBILE_BOOST_TEST_APK)
       - Module [MOBILE_DLL](#module_MOBILE_DLL)
       - Module [MOBILE_LIBRARY](#module_MOBILE_LIBRARY)
       - Module [MOBILE_TEST_APK](#module_MOBILE_TEST_APK)
       - Module [NPM_CONTRIBS](#module_NPM_CONTRIBS)
       - Module [PACKAGE](#module_PACKAGE)
       - Module [PREBUILT_PROGRAM](#module_PREBUILT_PROGRAM)
       - Module [PROGRAM](#module_PROGRAM)
       - Module [PROTO_DESCRIPTIONS](#module_PROTO_DESCRIPTIONS)
       - Module [PROTO_REGISTRY](#module_PROTO_REGISTRY)
       - Module [PY2MODULE](#module_PY2MODULE)
       - Module [PY2TEST](#module_PY2TEST)
       - Module [PY2_LIBRARY](#module_PY2_LIBRARY)
       - Module [PY2_PROGRAM](#module_PY2_PROGRAM)
       - Module [PY3MODULE](#module_PY3MODULE)
       - Module [PY3TEST_BIN](#module_PY3TEST_BIN)
       - Module [PY3_LIBRARY](#module_PY3_LIBRARY)
       - Module [PY3_PROGRAM_BIN](#module_PY3_PROGRAM_BIN)
       - Module [PYTEST_BIN](#module_PYTEST_BIN)
       - Module [PY_ANY_MODULE](#module_PY_ANY_MODULE)
       - Module [PY_PACKAGE](#module_PY_PACKAGE)
       - Module [RECURSIVE_LIBRARY](#module_RECURSIVE_LIBRARY)
       - Module [RESOURCES_LIBRARY](#module_RESOURCES_LIBRARY)
       - Module [R_MODULE](#module_R_MODULE)
       - Module [SO_PROGRAM](#module_SO_PROGRAM)
       - Module [TS_BUNDLE](#module_TS_BUNDLE)
       - Module [TS_LIBRARY](#module_TS_LIBRARY)
       - Module [TS_TEST](#module_TS_TEST)
       - Module [UDF_BASE](#module_UDF_BASE)
       - Module [UNION](#module_UNION)
       - Module [UNITTEST](#module_UNITTEST)
       - Module [UNITTEST_FOR](#module_UNITTEST_FOR)
       - Module [UNITTEST_WITH_CUSTOM_ENTRY_POINT](#module_UNITTEST_WITH_CUSTOM_ENTRY_POINT)
       - Module [YQL_PYTHON3_UDF](#module_YQL_PYTHON3_UDF)
       - Module [YQL_PYTHON3_UDF_TEST](#module_YQL_PYTHON3_UDF_TEST)
       - Module [YQL_PYTHON_UDF](#module_YQL_PYTHON_UDF)
       - Module [YQL_PYTHON_UDF_PROGRAM](#module_YQL_PYTHON_UDF_PROGRAM)
       - Module [YQL_PYTHON_UDF_TEST](#module_YQL_PYTHON_UDF_TEST)
       - Module [YQL_UDF_MODULE](#module_YQL_UDF_MODULE)
       - Module [YQL_UDF_TEST](#module_YQL_UDF_TEST)
       - Module [YT_UNITTEST](#module_YT_UNITTEST)
       - Module [Y_BENCHMARK](#module_Y_BENCHMARK)
       - Module [_BARE_UNIT](#module__BARE_UNIT)
       - Module [_BASE_PROGRAM](#module__BASE_PROGRAM)
       - Module [_BASE_PY3_PROGRAM](#module__BASE_PY3_PROGRAM)
       - Module [_BASE_PYTEST](#module__BASE_PYTEST)
       - Module [_BASE_PY_PROGRAM](#module__BASE_PY_PROGRAM)
       - Module [_BASE_UNIT](#module__BASE_UNIT)
       - Module [_BASE_UNITTEST](#module__BASE_UNITTEST)
       - Module [_COMPILABLE_JAR_BASE](#module__COMPILABLE_JAR_BASE)
       - Module [_DLL_COMPATIBLE_LIBRARY](#module__DLL_COMPATIBLE_LIBRARY)
       - Module [_DOCS_BARE_UNIT](#module__DOCS_BARE_UNIT)
       - Module [_DOCS_BASE_UNIT](#module__DOCS_BASE_UNIT)
       - Module [_GO_BASE_UNIT](#module__GO_BASE_UNIT)
       - Module [_GO_DLL_BASE_UNIT](#module__GO_DLL_BASE_UNIT)
       - Module [_JAR_BASE](#module__JAR_BASE)
       - Module [_JAR_RUNNABLE](#module__JAR_RUNNABLE)
       - Module [_JAR_TEST](#module__JAR_TEST)
       - Module [_JAVA_PLACEHOLDER](#module__JAVA_PLACEHOLDER)
       - Module [_LIBRARY](#module__LIBRARY)
       - Module [_LINK_UNIT](#module__LINK_UNIT)
       - Module [_MKDOCS_BASE_UNIT](#module__MKDOCS_BASE_UNIT)
       - Module [_PROXY_LIBRARY](#module__PROXY_LIBRARY)
       - Module [_PY2_PROGRAM](#module__PY2_PROGRAM)
       - Module [_PY_PACKAGE](#module__PY_PACKAGE)
       - Module [_TS_BASE_LIBRARY](#module__TS_BASE_LIBRARY)
       - Module [_TS_BASE_UNIT](#module__TS_BASE_UNIT)
       - Module [_YQL_UDF_PROGRAM_BASE](#module__YQL_UDF_PROGRAM_BASE)
   * [Macros](#macros)
       - Macros [AARS](#macro_AARS) .. [AAR_LOCAL_MAVEN_REPO](#macro_AAR_LOCAL_MAVEN_REPO)
       - Macros [AAR_MANIFEST](#macro_AAR_MANIFEST) .. [ADD_COMPILABLE_TRANSLATE](#macro_ADD_COMPILABLE_TRANSLATE)
       - Macros [ADD_COMPILABLE_TRANSLIT](#macro_ADD_COMPILABLE_TRANSLIT) .. [ALL_RESOURCE_FILES](#macro_ALL_RESOURCE_FILES)
       - Macros [ALL_SRCS](#macro_ALL_SRCS) .. [BISON_FLAGS](#macro_BISON_FLAGS)
       - Macros [BISON_GEN_C](#macro_BISON_GEN_C) .. [BUILD_CATBOOST](#macro_BUILD_CATBOOST)
       - Macros [BUILD_MN](#macro_BUILD_MN) .. [BUNDLE_RES_SRCS](#macro_BUNDLE_RES_SRCS)
       - Macros [CFG_VARS](#macro_CFG_VARS) .. [CHECK_JAVA_DEPS](#macro_CHECK_JAVA_DEPS)
       - Macros [CLANG_EMIT_AST_CXX](#macro_CLANG_EMIT_AST_CXX) .. [COMPILE_NLG](#macro_COMPILE_NLG)
       - Macros [COMPILE_SWIFT_MODULE](#macro_COMPILE_SWIFT_MODULE) .. [CPP_PROTO_PLUGIN](#macro_CPP_PROTO_PLUGIN)
       - Macros [CPP_PROTO_PLUGIN0](#macro_CPP_PROTO_PLUGIN0) .. [DARWIN_SIGNED_RESOURCE](#macro_DARWIN_SIGNED_RESOURCE)
       - Macros [DARWIN_STRINGS_RESOURCE](#macro_DARWIN_STRINGS_RESOURCE) .. [DEFAULT](#macro_DEFAULT)
       - Macros [DEPENDENCY_MANAGEMENT](#macro_DEPENDENCY_MANAGEMENT) .. [DOCS_INCLUDE_SOURCES](#macro_DOCS_INCLUDE_SOURCES)
       - Macros [DOCS_VARS](#macro_DOCS_VARS) .. [END](#macro_END)
       - Macros [ENDIF](#macro_ENDIF) .. [EXTERNAL_JAR](#macro_EXTERNAL_JAR)
       - Macros [EXTERNAL_RESOURCE](#macro_EXTERNAL_RESOURCE) .. [FLAT_JOIN_SRCS_GLOBAL](#macro_FLAT_JOIN_SRCS_GLOBAL)
       - Macros [FLEX_FLAGS](#macro_FLEX_FLAGS) .. [FROM_NPM_LOCKFILES](#macro_FROM_NPM_LOCKFILES)
       - Macros [FROM_SANDBOX](#macro_FROM_SANDBOX) .. [GLOBAL_SRCS](#macro_GLOBAL_SRCS)
       - Macros [GOLANG_VERSION](#macro_GOLANG_VERSION) .. [GO_EMBED_XTEST_DIR](#macro_GO_EMBED_XTEST_DIR)
       - Macros [GO_FAKE_OUTPUT](#macro_GO_FAKE_OUTPUT) .. [GO_PACKAGE_NAME](#macro_GO_PACKAGE_NAME)
       - Macros [GO_PROTO_PLUGIN](#macro_GO_PROTO_PLUGIN) .. [IDEA_EXCLUDE_DIRS](#macro_IDEA_EXCLUDE_DIRS)
       - Macros [IDEA_JAR_SRCS](#macro_IDEA_JAR_SRCS) .. [IOS_APP_COMMON_FLAGS](#macro_IOS_APP_COMMON_FLAGS)
       - Macros [IOS_APP_SETTINGS](#macro_IOS_APP_SETTINGS) .. [JAVA_IGNORE_CLASSPATH_CLASH_FOR](#macro_JAVA_IGNORE_CLASSPATH_CLASH_FOR)
       - Macros [JAVA_MODULE](#macro_JAVA_MODULE) .. [JVM_ARGS](#macro_JVM_ARGS)
       - Macros [KAPT_ANNOTATION_PROCESSOR](#macro_KAPT_ANNOTATION_PROCESSOR) .. [LINK_EXEC_DYN_LIB_IMPL](#macro_LINK_EXEC_DYN_LIB_IMPL)
       - Macros [LINK_EXE_IMPL](#macro_LINK_EXE_IMPL) .. [LLVM_OPT](#macro_LLVM_OPT)
       - Macros [LOCAL_JAR](#macro_LOCAL_JAR) .. [MAPSMOBI_COLLECT_JAVA_FILES](#macro_MAPSMOBI_COLLECT_JAVA_FILES)
       - Macros [MAPSMOBI_COLLECT_JNI_LIBS_FILES](#macro_MAPSMOBI_COLLECT_JNI_LIBS_FILES) .. [MAVEN_GROUP_ID](#macro_MAVEN_GROUP_ID)
       - Macros [MESSAGE](#macro_MESSAGE) .. [NEED_REVIEW](#macro_NEED_REVIEW)
       - Macros [NGINX_MODULES](#macro_NGINX_MODULES) .. [NO_CYTHON_COVERAGE](#macro_NO_CYTHON_COVERAGE)
       - Macros [NO_DEBUG_INFO](#macro_NO_DEBUG_INFO) .. [NO_NEED_CHECK](#macro_NO_NEED_CHECK)
       - Macros [NO_OPTIMIZE](#macro_NO_OPTIMIZE) .. [NO_SSE4](#macro_NO_SSE4)
       - Macros [NO_UTIL](#macro_NO_UTIL) .. [PACK](#macro_PACK)
       - Macros [PACKAGE_STRICT](#macro_PACKAGE_STRICT) .. [PRIMARY_OUTPUT](#macro_PRIMARY_OUTPUT)
       - Macros [PRINT_MODULE_TYPE](#macro_PRINT_MODULE_TYPE) .. [PYTHON2_ADDINCL](#macro_PYTHON2_ADDINCL)
       - Macros [PYTHON2_MODULE](#macro_PYTHON2_MODULE) .. [PY_NAMESPACE](#macro_PY_NAMESPACE)
       - Macros [PY_PROTOS_FOR](#macro_PY_PROTOS_FOR) .. [RECURSE](#macro_RECURSE)
       - Macros [RECURSE_FOR_TESTS](#macro_RECURSE_FOR_TESTS) .. [RESTRICT_LICENSES](#macro_RESTRICT_LICENSES)
       - Macros [RESTRICT_PATH](#macro_RESTRICT_PATH) .. [RUN_PROGRAM](#macro_RUN_PROGRAM)
       - Macros [RUN_PYTHON3](#macro_RUN_PYTHON3) .. [SET_APPEND_WITH_GLOBAL](#macro_SET_APPEND_WITH_GLOBAL)
       - Macros [SET_COMPILE_OUTPUTS_MODIFIERS](#macro_SET_COMPILE_OUTPUTS_MODIFIERS) .. [SRC](#macro_SRC)
       - Macros [SRCDIR](#macro_SRCDIR) .. [SRC_C_SSE3](#macro_SRC_C_SSE3)
       - Macros [SRC_C_SSE4](#macro_SRC_C_SSE4) .. [SUBSCRIBER](#macro_SUBSCRIBER)
       - Macros [SUPPRESSIONS](#macro_SUPPRESSIONS) .. [TEST_JAVA_CLASSPATH_CMD_TYPE](#macro_TEST_JAVA_CLASSPATH_CMD_TYPE)
       - Macros [TEST_SRCS](#macro_TEST_SRCS) .. [UBERJAR_HIDING_PREFIX](#macro_UBERJAR_HIDING_PREFIX)
       - Macros [UBERJAR_MANIFEST_TRANSFORMER_ATTRIBUTE](#macro_UBERJAR_MANIFEST_TRANSFORMER_ATTRIBUTE) .. [USE_ERROR_PRONE](#macro_USE_ERROR_PRONE)
       - Macros [USE_EXT_PROTO](#macro_USE_EXT_PROTO) .. [USE_PYTHON2](#macro_USE_PYTHON2)
       - Macros [USE_PYTHON3](#macro_USE_PYTHON3) .. [WINDOWS_MANIFEST](#macro_WINDOWS_MANIFEST)
       - Macros [WITHOUT_LICENSE_TEXTS](#macro_WITHOUT_LICENSE_TEXTS) .. [WITH_KOTLINC_SERIALIZATION](#macro_WITH_KOTLINC_SERIALIZATION)
       - Macros [XSTYPEMAPS](#macro_XSTYPEMAPS) .. [YQL_ABI_VERSION](#macro_YQL_ABI_VERSION)
       - Macros [YQL_LAST_ABI_VERSION](#macro_YQL_LAST_ABI_VERSION) .. [_ADD_HIDDEN_INPUTS](#macro__ADD_HIDDEN_INPUTS)
       - Macros [_ADD_JAVA_STYLE_CHECKS](#macro__ADD_JAVA_STYLE_CHECKS) .. [_ARCADIA_PYTHON_ADDINCL](#macro__ARCADIA_PYTHON_ADDINCL)
       - Macros [_ARCHIVE_SEM_HELPER](#macro__ARCHIVE_SEM_HELPER) .. [_BUILD_MNS_CPP](#macro__BUILD_MNS_CPP)
       - Macros [_BUILD_MNS_FILE](#macro__BUILD_MNS_FILE) .. [_COPY_FILE_IMPL](#macro__COPY_FILE_IMPL)
       - Macros [_CPP_CFGPROTO_CMD](#macro__CPP_CFGPROTO_CMD) .. [_DOCS_MKDOCS_CMD_IMPL](#macro__DOCS_MKDOCS_CMD_IMPL)
       - Macros [_DOCS_SRCS](#macro__DOCS_SRCS) .. [_FETCH_CONTRIB](#macro__FETCH_CONTRIB)
       - Macros [_FILL_JAR_COPY_RESOURCES_CMD](#macro__FILL_JAR_COPY_RESOURCES_CMD) .. [_GEN_JAVA_SCRIPT_IMPL](#macro__GEN_JAVA_SCRIPT_IMPL)
       - Macros [_GLOB](#macro__GLOB) .. [_GO_GRPC_GATEWAY_SRCS](#macro__GO_GRPC_GATEWAY_SRCS)
       - Macros [_GO_GRPC_GATEWAY_SRCS_IMPL](#macro__GO_GRPC_GATEWAY_SRCS_IMPL) .. [_GO_SRCS](#macro__GO_SRCS)
       - Macros [_GO_UNUSED_SRCS](#macro__GO_UNUSED_SRCS) .. [_JAVA_FLATC_CMD](#macro__JAVA_FLATC_CMD)
       - Macros [_JAVA_PROTO_CMD](#macro__JAVA_PROTO_CMD) .. [_MAKE_YQL_PYTHON_UDF_TEST](#macro__MAKE_YQL_PYTHON_UDF_TEST)
       - Macros [_MAKE_YQL_UDF](#macro__MAKE_YQL_UDF) .. [_MOBILE_TEST_APK_CMD_IMPL](#macro__MOBILE_TEST_APK_CMD_IMPL)
       - Macros [_MSVC_FLAGS_WINDOWS_IMPL](#macro__MSVC_FLAGS_WINDOWS_IMPL) .. [_PY3_COMPILE_BYTECODE](#macro__PY3_COMPILE_BYTECODE)
       - Macros [_PY3_REGISTER](#macro__PY3_REGISTER) .. [_PY_PROGRAM](#macro__PY_PROGRAM)
       - Macros [_PY_PROTO_CMD](#macro__PY_PROTO_CMD) .. [_REGISTER_NO_CHECK_IMPORTS](#macro__REGISTER_NO_CHECK_IMPORTS)
       - Macros [_REQUIRE_EXPLICIT_LICENSE](#macro__REQUIRE_EXPLICIT_LICENSE) .. [_SPLIT_CODEGEN_BASE](#macro__SPLIT_CODEGEN_BASE)
       - Macros [_SRC](#macro__SRC) .. [_SRC_C_CUSTOM_FLAGS](#macro__SRC_C_CUSTOM_FLAGS)
       - Macros [_SRC_STRICT_C_CPP](#macro__SRC_STRICT_C_CPP) .. [_SRC____asp](#macro__SRC____asp)
       - Macros [_SRC____c](#macro__SRC____c) .. [_SRC____fbs64](#macro__SRC____fbs64)
       - Macros [_SRC____fml](#macro__SRC____fml) .. [_SRC____lua](#macro__SRC____lua)
       - Macros [_SRC____m](#macro__SRC____m) .. [_SRC____rl5](#macro__SRC____rl5)
       - Macros [_SRC____rl6](#macro__SRC____rl6) .. [_SRC____xib](#macro__SRC____xib)
       - Macros [_SRC____xs](#macro__SRC____xs) .. [_SRC_lua_21](#macro__SRC_lua_21)
       - Macros [_SRC_m](#macro__SRC_m) .. [_TARGET_SOURCES_FOR_HEADERS](#macro__TARGET_SOURCES_FOR_HEADERS)
       - Macros [_TARGET_SOURCES_FOR_HEADERS_IMPL](#macro__TARGET_SOURCES_FOR_HEADERS_IMPL) .. [_YFM_DOCS_DIR](#macro__YFM_DOCS_DIR)
       - Macros [_YMAKE_GENERATE_SCRIPT](#macro__YMAKE_GENERATE_SCRIPT) .. [_YTEST](#macro__YTEST)
## Multimodules <a name="multimodules"></a>

###### Multimodule [DLL\_JAVA][]() <a name="multimodule_DLL_JAVA"></a>
DLL built using swig for Java. Produces dynamic library and a .jar.
Dynamic library is treated the same as in the case of PEERDIR from Java to DLL.
.jar goes on the classpath.

Documentation: https://wiki.yandex-team.ru/yatool/java/#integracijascpp/pythonsborkojj

###### Multimodule [DOCS][]() <a name="multimodule_DOCS"></a>
Documentation project multimodule.

When built directly, via RECURSE, DEPENDS or BUNDLE the output artifact is docs.tar.gz with statically generated site.
When PEERDIRed from other DOCS() module behaves like a UNION (supplying own content and dependencies to build target).
Peerdirs from modules other than DOCS are not accepted.
Most usual macros are not accepted, only used with the macros DOCS\_DIR(), DOCS\_CONFIG(), DOCS\_VARS().

@see: [DOCS\_DIR()](#macro\_DOCS\_DIR), [DOCS\_CONFIG()](#macro\_DOCS\_CONFIG), [DOCS\_VARS()](#macro\_DOCS\_VARS).

###### Multimodule [DYNAMIC\_LIBRARY][]() _# internal_ <a name="multimodule_DYNAMIC_LIBRARY"></a>
The use of this module is strictly prohibited except LGPL-related opensourcing
This provides linkable DLL module which brings its results to programs and tests
for seamless testing and packaging

###### Multimodule [FBS\_LIBRARY][]() <a name="multimodule_FBS_LIBRARY"></a>
Build some variant of Flatbuffers library.

The particular variant is selected based on where PEERDIR to FBS\_LIBRARY
comes from.

Now supported 5 variants: C++, Java, Python 2.x, Python 3.x and Go.
When PEERDIR comes from module for particular language appropriate variant
is selected.

Notes: FBS\_NAMESPACE must be specified in all dependent FBS\_LIBRARY modules
       if build of Go code is requested.

###### Multimodule [JAR\_PROGRAM][] <a name="multimodule_JAR_PROGRAM"></a>
Not documented yet.

###### Multimodule [JAVA\_CONTRIB\_PROGRAM][] <a name="multimodule_JAVA_CONTRIB_PROGRAM"></a>
Not documented yet.

###### Multimodule [JAVA\_PROGRAM][]() <a name="multimodule_JAVA_PROGRAM"></a>
The module describing java programs build.
Output artifacts: .jar and directory with all the jar to the classpath of the formation.

Documentation: https://wiki.yandex-team.ru/yatool/java/

###### Multimodule [JTEST][] <a name="multimodule_JTEST"></a>
Not documented yet.

###### Multimodule [JTEST\_FOR][] <a name="multimodule_JTEST_FOR"></a>
Not documented yet.

###### Multimodule [JTEST\_YMAKE][] <a name="multimodule_JTEST_YMAKE"></a>
Not documented yet.

###### Multimodule [JUNIT5][] <a name="multimodule_JUNIT5"></a>
Not documented yet.

###### Multimodule [JUNIT5\_YMAKE][] <a name="multimodule_JUNIT5_YMAKE"></a>
Not documented yet.

###### Multimodule [MAPS\_IDL\_LIBRARY][]() <a name="multimodule_MAPS_IDL_LIBRARY"></a>
Definition of multimodule that builds various variants of libraries.
The particular variant is selected based on where PEERDIR to IDL\_LIBRARY comes from.
Now supported 2 variants: C++, Java
Java version is not really a library but an archive of generated Java sources

###### Multimodule [MKDOCS][]() <a name="multimodule_MKDOCS"></a>
Documentation project multimodule.

When built directly, via RECURSE, DEPENDS or BUNDLE the output artifact is docs.tar.gz with statically generated site (using mkdocs as builder).
When PEERDIRed from other MKDOCS() module behaves like a UNION (supplying own content and dependencies to build target).
Peerdirs from modules other than MKDOCS are not accepted.
Most usual macros are not accepted, only used with the macros DOCS\_DIR(), DOCS\_CONFIG(), DOCS\_VARS().

@see: [DOCS\_DIR()](#macro\_DOCS\_DIR), [DOCS\_CONFIG()](#macro\_DOCS\_CONFIG), [DOCS\_VARS()](#macro\_DOCS\_VARS).

###### Multimodule [PROTO\_LIBRARY][]() <a name="multimodule_PROTO_LIBRARY"></a>
Build some varian of protocol buffers library.

The particular variant is selected based on where PEERDIR to PROTO\_LIBRARY comes from.

Now supported 5 variants: C++, Java, Python 2.x, Python 3.x and Go.
When PEERDIR comes from module for particular language appropriate variant is selected.
PROTO\_LIBRARY also supports emission of GRPC code if GRPC() macro is specified.
Notes:
- Python versions emit C++ code in addition to Python as optimization.
- In some PROTO\_LIBRARY-es Java or Python versions are excluded via EXCLUDE\_TAGS macros due to incompatibilities.
- Use from DEPENDS or BUNDLE is not allowed

Documentation: https://wiki.yandex-team.ru/yatool/proto\_library/

See: [GRPC()](#macro\_GRPC), [OPTIMIZE\_PY\_PROTOS()](#macro\_OPTIMIZE\_PY\_PROTOS), [INCLUDE\_TAGS()](#macro\_INCLUDE\_TAGS), [EXCLUDE\_TAGS()](#macro\_EXCLUDE\_TAGS)

###### Multimodule [PY23\_LIBRARY][]([name]) <a name="multimodule_PY23_LIBRARY"></a>
Build PY2\_LIBRARY or PY3\_LIBRARY depending on incoming PEERDIR.
Direct build or build by RECURSE creates both variants.
This multimodule doesn't define any final targets, so use from DEPENDS or BUNDLE is not allowed.

Documentation: https://wiki.yandex-team.ru/arcadia/python/pysrcs

###### Multimodule [PY23\_NATIVE\_LIBRARY][]([name]) <a name="multimodule_PY23_NATIVE_LIBRARY"></a>
Build LIBRARY compatible with either Python 2.x or Python 3.x depending on incoming PEERDIR.

This multimodule doesn't depend on Arcadia Python binary build. It is intended only for C++ code and cannot contain PY\_SRCS and USE\_PYTHON2 macros.
Use these multimodule instead of PY23\_LIBRARY if the C++ extension defined in it will be used in PY2MODULE.
While it doesn't bring Arcadia Python dependency itself, it is still compatible with Arcadia Python build and can be PEERDIR-ed from PY2\_LIBRARY and alikes.
Proper version will be selected according to Python version of the module PEERDIR comes from.

This mulrtimodule doesn't define any final targets so cannot be used from DEPENDS or BUNDLE macros.

For more information read https://wiki.yandex-team.ru/arcadia/python/pysrcs/#pysrcssrcsipy23nativelibrary

@see [LIBRARY()](#module\_LIBRARY), [PY2MODULE()](#module\_PY2MODULE)

###### Multimodule [PY23\_TEST][] <a name="multimodule_PY23_TEST"></a>
Not documented yet.

###### Multimodule [PY3TEST][]([name]) <a name="multimodule_PY3TEST"></a>
The test module for Python 3.x based on py.test

This module is compatible only with PYTHON3-tagged modules and selects peers from multimodules accordingly.
This module is only compatible with Arcadia Python build (to avoid tests duplication from Python2/3-tests). For non-Arcadia python use PYTEST.

Documentation: https://wiki.yandex-team.ru/yatool/test/#testynapytest
Documentation about the Arcadia test system: https://wiki.yandex-team.ru/yatool/test/

###### Multimodule [PY3\_PROGRAM][]([progname]) <a name="multimodule_PY3_PROGRAM"></a>
Python 3.x binary program. Links all Python 3.x libraries and Python 3.x interpreter into itself to form regular executable.
If name is not specified it will be generated from the name of the containing project directory.
This only compatible with PYTHON3-tagged modules and selects those from multimodules.

Documentation: https://wiki.yandex-team.ru/devtools/commandsandvars/py\_srcs/

###### Multimodule [SANDBOX\_PY23\_TASK][] <a name="multimodule_SANDBOX_PY23_TASK"></a>
Not documented yet.

###### Multimodule [SANDBOX\_PY3\_TASK][]([Name]) <a name="multimodule_SANDBOX_PY3_TASK"></a>
Multimodule describing Sandbox task (Python3 code that can be executed by Sandbox system).

When being a final target, this multimodule builds Sandbox binary task. It may PEERDIR other SANDBOX\_PY3\_TASKs as libraries.
The final artifact is provided when SANDBOX\_PY3\_TASK is referred to by DEPENDS and BUNDLE macros.
As PEERDIR target, it works like regular PY3\_LIBRARY with predefined dependencies on Sandbox SDK to allow code reuse among SANDBOX\_PY3\_TASKs.

Currently Sandbox supports Python 3.x only in binary tasks, both variants will be compatible only with Python 3.x and py23 libraries
and will select multimodule variants accordingly.

Documentation: https://wiki.yandex-team.ru/sandbox/tasks/binary

###### Multimodule [SANDBOX\_TASK][]([Name]) <a name="multimodule_SANDBOX_TASK"></a>
Multimodule describing Sandbox task (Python code that can be executed by Sandbox system).

When being a final target, this multimodule builds Sandbox binary task. It may PEERDIR other SANDBOX\_TASKs as libraries.
The final artifact is provided when SANDBOX\_TASK is referred to by DEPENDS and BUNDLE macros.
As PEERDIR target, it works like regular PY2\_LIBRARY with predefined dependencies on Sandbox SDK to allow code reuse among SANDBOX\_TASKs.

Currently Sandbox supports only Python 2.x, so both variants will be compatible only with Python 2.x modules
and will select multimodule variants accordingly.

Documentation: https://wiki.yandex-team.ru/sandbox/tasks/binary

###### Multimodule [SSQLS\_LIBRARY][] <a name="multimodule_SSQLS_LIBRARY"></a>
Not documented yet.

###### Multimodule [YQL\_UDF][](name) <a name="multimodule_YQL_UDF"></a>
User-defined function for YQL

Multimodule which is YQL\_UDF\_MODULE when built directly or referred by BUNDLE and DEPENDS macros.
If used by PEERDIRs it is usual static LIBRARY with default YQL dependencies, allowing code reuse between UDFs.

@see: [YQL\_UDF\_MODULE()](#module\_YQL\_UDF\_MODULE)

## Modules <a name="modules"></a>

###### Module [AAR][]() _# internal_ <a name="module_AAR"></a>
Not documented yet.

###### Module [AAR\_PROXY\_LIBRARY][]() _# internal_ <a name="module_AAR_PROXY_LIBRARY"></a>
The use of this module is strictly prohibited!!!

###### Module [ASRC\_LIBRARY][]() _# internal_ <a name="module_ASRC_LIBRARY"></a>
Not documented yet.

###### Module [BOOSTTEST][]([name]) _#deprecated_ <a name="module_BOOSTTEST"></a>
Test module based on boost/test/unit\_test.hpp.
As with entire boost library usage of this technology is deprecated in Arcadia and restricted with configuration error in most of projects.
No new module of this type should be introduced unless it is explicitly approved by C++ committee.

###### Module [BOOSTTEST\_WITH\_MAIN][]([name]) _#deprecated_ <a name="module_BOOSTTEST_WITH_MAIN"></a>
Same as BOOSTTEST (see above), but comes with builtin int main(argc, argv) implementation

###### Module [CI\_GROUP][]() <a name="module_CI_GROUP"></a>
Module collects what is described directly inside it transitively by PEERDIRs.
No particular layout of built artifacts is implied. This module is needed primarily for CI dependency analysis and may not trigger builds at all.

Is only used together with the macro PEERDIR() and FILES(). Don't use SRCS inside CI\_GROUP().

###### Module [CONTAINER][]: \_BARE\_UNIT <a name="module_CONTAINER"></a>
Not documented yet.

###### Module [CONTAINER\_LAYER][]: \_BARE\_UNIT <a name="module_CONTAINER_LAYER"></a>
Not documented yet.

###### Module [CPP\_STYLE\_TEST][]: PY3TEST\_BIN <a name="module_CPP_STYLE_TEST"></a>
Not documented yet.

###### Module [CUSTOM\_BUILD\_LIBRARY][]: LIBRARY <a name="module_CUSTOM_BUILD_LIBRARY"></a>
Not documented yet.

###### Module [DEFAULT\_IOS\_INTERFACE][]: IOS\_INTERFACE <a name="module_DEFAULT_IOS_INTERFACE"></a>
Not documented yet.

###### Module [DEV\_DLL\_PROXY][]() _# internal_ <a name="module_DEV_DLL_PROXY"></a>
The use of this module is strictly prohibited!!!
This is a temporary and project-specific solution.

###### Module [DLL][](name major\_ver [minor\_ver] [EXPORTS symlist\_file] [PREFIX prefix]) <a name="module_DLL"></a>
Dynamic library module definition.
1. major\_ver and minor\_ver must be integers.
2. EXPORTS allows you to explicitly specify the list of exported functions. This accepts 2 kind of files: .exports with <lang symbol> pairs and JSON-line .symlist files
3. PREFIX allows you to change the prefix of the output file (default DLL has the prefix "lib").

DLL cannot participate in linking to programs but can be used from Java or as final artifact (packaged and deployed).

###### Module [DLL\_PROXY][]() _# internal_ <a name="module_DLL_PROXY"></a>
The use of this module is strictly prohibited!!!
This is a temporary and project-specific solution.

###### Module [DLL\_PROXY\_LIBRARY][]() _# internal_ <a name="module_DLL_PROXY_LIBRARY"></a>
The use of this module is strictly prohibited!!!

###### Module [DLL\_TOOL][] <a name="module_DLL_TOOL"></a>
DLL\_TOOL is a DLL that can be used as a LD\_PRELOAD tool.

###### Module [DLL\_UNIT][] _# internal_ <a name="module_DLL_UNIT"></a>
Base module for all dynamically linked libraries as final artifacts.
Contains all general logic for such kind of modules. Supports versioning and export files.
Cannot participate in linking to programs, intended to be used as final artifact (packaged and deployed).

###### Module [DOCS\_LIBRARY][]: \_DOCS\_BARE\_UNIT <a name="module_DOCS_LIBRARY"></a>
Not documented yet.

###### Module [EXECTEST][]() <a name="module_EXECTEST"></a>
Module definition of generic test that executes a binary.
Use macro RUN to specify binary to run.

@example:

    EXECTEST()
        OWNER(g:yatool)

        RUN(
            cat input.txt
        )
        DATA(
            arcadia/devtools/ya/test/tests/exectest/data
        )
        DEPENDS(
            devtools/dummy_arcadia/cat
        )
        TEST_CWD(devtools/ya/test/tests/exectest/data)
    END()

More examples: https://wiki.yandex-team.ru/yatool/test/#exec-testy

@see: [RUN()](#macro\_RUN)

###### Module [EXTERNAL\_JAVA\_LIBRARY][]() _#internal_ <a name="module_EXTERNAL_JAVA_LIBRARY"></a>
EXTERNAL\_JAVA\_LIBRARY() is a module for creating a .jar file using non-Java code (generators etc.)
Unlike regular JAVA\_LIBRARY this module doesn't produce .pom file, so it cannot be exported to Maven itself.
PEERDIR it from JAVA\_LIBRARY or JAVA\_PROGRAM for export to Maven.

###### Module [FAT\_OBJECT][]() <a name="module_FAT_OBJECT"></a>
The "fat" object module. It will contain all its transitive dependencies reachable by PEERDIRs:
static libraries, local (from own SRCS) and global (from peers') object files.

Designed for use in XCode projects for iOS.

###### Module [FUZZ][]() <a name="module_FUZZ"></a>
In order to start using Fuzzing in Arcadia, you need to create a FUZZ module with the implementation of the function LLVMFuzzerTestOneInput().
This module should be reachable by RECURSE from /autocheck project in order for the corpus to be regularly updated.
AFL and Libfuzzer are supported in Arcadia via a single interface, but the automatic fuzzing still works only through Libfuzzer.

Example: https://a.yandex-team.ru/arc/trunk/arcadia/contrib/libs/re2/re2/fuzzing/re2\_fuzzer.cc?rev=2919463#L58

Documentation: https://wiki.yandex-team.ru/yatool/fuzzing/

###### Module [GO\_DLL][](name major\_ver [minor\_ver] [PREFIX prefix]) <a name="module_GO_DLL"></a>
Go ishared object module definition.
Compile and link Go module to a shared object.
Will select Go implementation on PEERDIR to PROTO\_LIBRARY.

###### Module [GO\_LIBRARY][]([name]) <a name="module_GO_LIBRARY"></a>
Go library module definition.
Compile Go module as a library suitable for PEERDIR from other Go modules.
Will select Go implementation on PEERDIR to PROTO\_LIBRARY.

###### Module [GO\_PROGRAM][]([name]) <a name="module_GO_PROGRAM"></a>
Go program module definition.
Compile and link Go module to an executable program.
Will select Go implementation on PEERDIR to PROTO\_LIBRARY.

###### Module [GO\_TEST][]([name]) <a name="module_GO_TEST"></a>
Go test module definition.
Compile and link Go module as a test suitable for running with Arcadia testing support.
All usual testing support macros like DATA, DEPENDS, SIZE, REQUIREMENTS etc. are supported.
Will select Go implementation on PEERDIR to PROTO\_LIBRARY.

###### Module [GTEST][]([name]) <a name="module_GTEST"></a>
Unit test module based on library/cpp/testing/gtest.
It is recommended not to specify the name.

Documentation: https://docs.yandex-team.ru/arcadia-cpp/cpp\_test

###### Module [GTEST\_UGLY][]([name]) <a name="module_GTEST_UGLY"></a>
Deprecated, do not use in new projects. Use GTEST instead.

The test module based on gtest (contrib/libs/gtest contrib/libs/gmock).
Use public documentation on gtest for details.

Documentation about the Arcadia test system: https://wiki.yandex-team.ru/yatool/test/

###### Module [G\_BENCHMARK][]([benchmarkname]) <a name="module_G_BENCHMARK"></a>
Benchmark test based on the google benchmark.

For more details see: https://a.yandex-team.ru/arc/trunk/arcadia/contrib/libs/benchmark/README.md

###### Module [IOS\_INTERFACE][]() <a name="module_IOS_INTERFACE"></a>
iOS GUI module definition

###### Module [JAR\_LIBRARY][]() _#internal_ <a name="module_JAR_LIBRARY"></a>
Reimplementation of the JAVA\_LIBRARY with ymake.core.conf and ymake based dependency management

###### Module [JAVA\_CONTRIB][]: \_JAR\_BASE <a name="module_JAVA_CONTRIB"></a>
Not documented yet.

###### Module [JAVA\_CONTRIB\_PROXY][]: \_JAR\_BASE <a name="module_JAVA_CONTRIB_PROXY"></a>
Not documented yet.

###### Module [JAVA\_LIBRARY][]() <a name="module_JAVA_LIBRARY"></a>
The module describing java library build.

Documentation: https://wiki.yandex-team.ru/yatool/java/

###### Module [JSRC\_LIBRARY][]() _# internal_ <a name="module_JSRC_LIBRARY"></a>
Not documented yet.

###### Module [JSRC\_PROXY\_MOBILE\_LIBRARY][]() _# internal_ <a name="module_JSRC_PROXY_MOBILE_LIBRARY"></a>
Not documented yet.

###### Module [LIBRARY][]() <a name="module_LIBRARY"></a>
The regular static library module.

The LIBRARY() is intermediate module, so when built directly it won't build its dependencies.
It transitively provides its PEERDIRs to ultimate final target, where all LIBRARY() modules are built and linked together.

This is C++ library, and it selects peers from multimodules accordingly.

It makes little sense to mention LIBRARY in DEPENDS or BUNDLE, package and deploy it since it is not a standalone entity.
In order to use library in tests PEERDIR it to link into tests.
If you think you need to distribute static library please contact devtools@ for assistance.

###### Module [MCU\_PROGRAM][]([progname]) <a name="module_MCU_PROGRAM"></a>
Program module for microcontrollers. Converts ELF to Intel HEX, Motorola S-record and raw binary file formats.
If name is not specified it will be generated from the name of the containing project directory.

###### Module [MOBILE\_BOOST\_TEST\_APK][]() _# internal_ <a name="module_MOBILE_BOOST_TEST_APK"></a>
Not documented yet.

###### Module [MOBILE\_DLL][]() _# internal_ <a name="module_MOBILE_DLL"></a>
Not documented yet.

###### Module [MOBILE\_LIBRARY][]() _# internal_ <a name="module_MOBILE_LIBRARY"></a>
Not documented yet.

###### Module [MOBILE\_TEST\_APK][]() _# internal_ <a name="module_MOBILE_TEST_APK"></a>
Not documented yet.

###### Module [NPM\_CONTRIBS][]() _# internal_ <a name="module_NPM_CONTRIBS"></a>
Defines special module that provides contrib tarballs from internal npm registry.
Should be used only with `NODE\_MODULES` macro.

@see [FROM\_NPM\_LOCKFILES()](#macro\_FROM\_NPM\_LOCKFILES)
@see [NODE\_MODULES()](#macro\_NODE\_MODULES)

###### Module [PACKAGE][](name) <a name="module_PACKAGE"></a>
Module collects what is described directly inside it, builds and collects all its transitively available PEERDIRs.
As a result, build directory of the project gets the structure of the accessible part of Arcadia, where the build result of each PEERDIR is placed to relevant Arcadia subpath.
The data can be optionally packed if macro PACK() is used.

Is only used together with the macros FILES(), PEERDIR(), COPY(), FROM\_SANDBOX(), RUN\_PROGRAM or BUNDLE(). Don't use SRCS inside a PACKAGE.

Documentation: https://wiki.yandex-team.ru/yatool/large-data/

@see: [PACK()](#macro\_PACK)

###### Module [PREBUILT\_PROGRAM][]([programname]) _# internal_ <a name="module_PREBUILT_PROGRAM"></a>
Program module which uses a prebuilt prgram as its output.

###### Module [PROGRAM][]([progname]) <a name="module_PROGRAM"></a>
Regular program module.
If name is not specified it will be generated from the name of the containing project directory.

###### Module [PROTO\_DESCRIPTIONS][]: \_BARE\_UNIT <a name="module_PROTO_DESCRIPTIONS"></a>
Not documented yet.

###### Module [PROTO\_REGISTRY][]: PROTO\_DESCRIPTIONS <a name="module_PROTO_REGISTRY"></a>
Not documented yet.

###### Module [PY2MODULE][](name major\_ver [minor\_ver] [EXPORTS symlist\_file] [PREFIX prefix]) <a name="module_PY2MODULE"></a>
The Python external module for Python2 and any system Python
1. major\_ver and minor\_ver must be integers.
2. The resulting .so will have the prefix "lib".
3. Processing EXPORTS and PREFIX is the same as for DLL module
This is native DLL, so it will select C++ version from PROTO\_LIBRARY.

Note: this module will always PEERDIR Python2 version of PY23\_NATIVE\_LIBRARY.
Do not PEERDIR PY2\_LIBRARY or PY23\_LIBRARY: this will link Python in and render artifact unusable as Python module.

Documentation: https://wiki.yandex-team.ru/devtools/commandsandvars/py\_srcs/

###### Module [PY2TEST][]([name]) <a name="module_PY2TEST"></a>
The test module for Python 2.x based on py.test

This module is compatible only with PYTHON2-tagged modules and selects peers from multimodules accordingly.
This module is compatible with non-Arcadia Python builds.

Documentation: https://wiki.yandex-team.ru/yatool/test/#python
Documentation about the Arcadia test system: https://wiki.yandex-team.ru/yatool/test/

###### Module [PY2\_LIBRARY][]() _# deprecated_ <a name="module_PY2_LIBRARY"></a>
Deprecated. Use PY23\_LIBRARY or PY3\_LIBRARY instead.
Python 2.x binary built library. Builds sources from PY\_SRCS to data suitable for PY2\_PROGRAM.
Adds dependencies to Python 2.x runtime library from Arcadia.
This module is only compatible with PYTHON2-tagged modules and selects those from multimodules.
This module is only compatible with Arcadia Python build.

Documentation: https://wiki.yandex-team.ru/devtools/commandsandvars/py\_srcs/

###### Module [PY2\_PROGRAM][]([progname]) _# deprecated_ <a name="module_PY2_PROGRAM"></a>
Deprecated. Use PY3\_PROGRAM instead.
Python 2.x binary program. Links all Python 2.x libraries and Python 2.x interpreter into itself to form regular executable.
If name is not specified it will be generated from the name of the containing project directory.
This only compatible with PYTHON2-tagged modules and selects those from multimodules.

Documentation: https://wiki.yandex-team.ru/devtools/commandsandvars/py\_srcs/

###### Module [PY3MODULE][](name major\_ver [minor\_ver] [EXPORTS symlist\_file] [PREFIX prefix]) <a name="module_PY3MODULE"></a>
The Python external module for Python3 and any system Python
1. major\_ver and minor\_ver must be integers.
2. The resulting .so will have the prefix "lib".
3. Processing EXPORTS and PREFIX is the same as for DLL module
This is native DLL, so it will select C++ version from PROTO\_LIBRARY.

Note: this module will always PEERDIR Python3 version of PY23\_NATIVE\_LIBRARY.
Do not PEERDIR PY3\_LIBRARY or PY23\_LIBRARY: this will link Python in and render artifact unusable as Python module.

Documentation: https://wiki.yandex-team.ru/devtools/commandsandvars/py\_srcs/

###### Module [PY3TEST\_BIN][]() _#deprecated_ <a name="module_PY3TEST_BIN"></a>
Same as PY3TEST. Don't use this, use PY3TEST instead.

###### Module [PY3\_LIBRARY][]() <a name="module_PY3_LIBRARY"></a>
Python 3.x binary library. Builds sources from PY\_SRCS to data suitable for PY2\_PROGRAM
Adds dependencies to Python 2.x runtime library from Arcadia.
This module is only compatible with PYTHON3-tagged modules and selects those from multimodules.
This module is only compatible with Arcadia Python build.

Documentation: https://wiki.yandex-team.ru/devtools/commandsandvars/py\_srcs/

###### Module [PY3\_PROGRAM\_BIN][]([progname]) <a name="module_PY3_PROGRAM_BIN"></a>
Use instead of PY3\_PROGRAM only if ya.make with PY3\_PROGRAM() included in another ya.make
In all other cases use PY3\_PROGRAM

###### Module [PYTEST\_BIN][]() _#deprecated_ <a name="module_PYTEST_BIN"></a>
Same as PY2TEST. Don't use this, use PY2TEST instead.

###### Module [PY\_ANY\_MODULE][](name major\_ver [minor\_ver] [EXPORTS symlist\_file] [PREFIX prefix]) <a name="module_PY_ANY_MODULE"></a>
The Python external module for any versio of Arcadia or system Python.
1. major\_ver and minor\_ver must be integers.
2. The resulting .so will have the prefix "lib".
3. Processing EXPORTS and PREFIX is the same as for DLL module
This is native DLL, so it will select C++ version from PROTO\_LIBRARY.

Note: Use PYTHON2\_MODULE()/PYTHON3\_MODULE() in order to PEERDIR proper version of PY23\_NATIVE\_LIBRARY.
Do not PEERDIR any PY\*\_LIBRARY: this will link Python in and render artifact unusable as Python module.

Documentation: https://wiki.yandex-team.ru/devtools/commandsandvars/py\_srcs/

###### Module [PY\_PACKAGE][](name) _# internal, deprecated_ <a name="module_PY_PACKAGE"></a>
This is module created via PY\_PROTOS\_FOR() macro

###### Module [RECURSIVE\_LIBRARY][]() <a name="module_RECURSIVE_LIBRARY"></a>
The recursive ("fat") library module. It will contain all its transitive dependencies reachable by PEERDIRs:
from static libraries, local (from own SRCS) and global (from peers') object files.

Designed for use in XCode projects for iOS.

###### Module [RESOURCES\_LIBRARY][]() <a name="module_RESOURCES_LIBRARY"></a>
Definition of a module that brings its content from external source (Sandbox) via DECLARE\_EXTERNAL\_RESOURCE macro.
This can participate in PEERDIRs of others as library but it cannot have own sources and PEERDIRs.

@see: [DECLARE\_EXTERNAL\_RESOURCE()](#macro\_DECLARE\_EXTERNAL\_RESOURCE)

###### Module [R\_MODULE][](name major\_ver [minor\_ver] [EXPORTS symlist\_file] [PREFIX prefix]) <a name="module_R_MODULE"></a>
The external module for R language.
1. major\_ver and minor\_ver must be integers.
2. The resulting .so will have the prefix "lib".
3. Processing EXPORTS and PREFIX is the same as for DLL module
This is native DLL, so it will select C++ version from PROTO\_LIBRARY.

###### Module [SO\_PROGRAM][](name major\_ver [minor\_ver] [EXPORTS symlist\_file] [PREFIX prefix]) <a name="module_SO_PROGRAM"></a>
Executable dynamic library module definition.
1. major\_ver and minor\_ver must be integers.
2. EXPORTS allows you to explicitly specify the list of exported functions. This accepts 2 kind of files: .exports with <lang symbol> pairs and JSON-line .symlist files
3. PREFIX allows you to change the prefix of the output file.

###### Module [TS\_BUNDLE][]([name]) <a name="module_TS_BUNDLE"></a>
The Webpack bundle, bundles JavaScript code.
Build results are bundle.tar, typings and source mappings (depending on local tsconfig.json settings).

@see [NODE\_MODULES()](#macro\_NODE\_MODULES)
@example

    TS_BUNDLE()
        SRCS(src/index.ts)
        NODE_MODULES()
    END()

###### Module [TS\_LIBRARY][]([name]) <a name="module_TS_LIBRARY"></a>
The TypeScript/JavaScript library module, compiles TypeScript sources to JavaScript.
Build results are JavaScript files, typings and source mappings (depending on local tsconfig.json settings).

@see [NODE\_MODULES()](#macro\_NODE\_MODULES)
@example

    TS_LIBRARY()
        SRCS(src/index.ts)
        NODE_MODULES()
    END()

###### Module [TS\_TEST][] <a name="module_TS_TEST"></a>
@see [TS\_TEST\_SRCS()](#macro\_TS\_TEST\_SRCS)
@see [TS\_TEST\_DATA()](#macro\_TS\_TEST\_DATA)

###### Module [UDF\_BASE][](name [EXPORTS symlist\_file] [PREFIX prefix]) _#internal_ <a name="module_UDF_BASE"></a>
The base logic of all UDF extension modules (User-Defined Functions).
Processing EXPORTS and PREFIX is the same as for DLL.

https://wiki.yandex-team.ru/robot/manual/kiwi/userguide/#polzovatelskiefunkciiudftriggerykwcalc

###### Module [UNION][](name) <a name="module_UNION"></a>
Collection of PEERDIR dependencies, files and artifacts.
UNION doesn't build its peers, just provides those to modules depending on it.
When specified in DEPENDS() macro the UNION is transitively closed, building all its peers and providing those by own paths (without adding this module path like PACKAGE does).

Is only used together with the macros like FILES(), PEERDIR(), COPY(), FROM\_SANDBOX(), RUN\_PROGRAM or BUNDLE(). Don't use SRCS inside a UNION.

Documentation: https://wiki.yandex-team.ru/yatool/large-data/

###### Module [UNITTEST][]([name]) <a name="module_UNITTEST"></a>
Unit test module based on library/cpp/testing/unittest.
It is recommended not to specify the name.

Documentation: https://wiki.yandex-team.ru/yatool/test/#opisanievya.make1

###### Module [UNITTEST\_FOR][](path/to/lib) <a name="module_UNITTEST_FOR"></a>
Convenience extension of UNITTEST module.
The UNINTTEST module with additional SRCDIR + ADDINCL + PEERDIR on path/to/lib.
path/to/lib is the path to the directory with the LIBRARY project.

Documentation about the Arcadia test system: https://wiki.yandex-team.ru/yatool/test/

###### Module [UNITTEST\_WITH\_CUSTOM\_ENTRY\_POINT][]([name]) <a name="module_UNITTEST_WITH_CUSTOM_ENTRY_POINT"></a>
Generic unit test module.

###### Module [YQL\_PYTHON3\_UDF][](name) <a name="module_YQL_PYTHON3_UDF"></a>
The extension module for YQL with Python 3.x UDF (User Defined Function for YQL).
Unlike YQL\_UDF this is plain DLL module, so PEERDIRs to it are not allowed.

Documentation: https://yql.yandex-team.ru/docs/yt/udf/python/

###### Module [YQL\_PYTHON3\_UDF\_TEST][](name) <a name="module_YQL_PYTHON3_UDF_TEST"></a>
The Python test for Python 3.x YQL UDF (User Defined Function for YQL). The code should be a proper YQL\_PYTHON3\_UDF.

This module will basically build itself as UDF and run as test using yql/tools/run\_python\_udf/run\_python\_udf tool.

Documentation: https://yql.yandex-team.ru/docs/yt/udf/python/

@see: [YQL\_PYTHON3\_UDF()](#module\_YQL\_PYTHON3\_UDF)

###### Module [YQL\_PYTHON\_UDF][](name) <a name="module_YQL_PYTHON_UDF"></a>
Definition of the extension module for YQL with Python 2.x UDF (User Defined Function for YQL).
Unlike YQL\_UDF this is plain DLL module, so PEERDIRs to it are not allowed.

https://yql.yandex-team.ru/docs/yt/udf/python/

###### Module [YQL\_PYTHON\_UDF\_PROGRAM][](name) <a name="module_YQL_PYTHON_UDF_PROGRAM"></a>
Definition of the extension module for YQL with Python 2.x UDF (User Defined Function for YQL).
Unlike YQL\_UDF this is plain DLL module, so PEERDIRs to it are not allowed.

https://yql.yandex-team.ru/docs/yt/udf/python/

###### Module [YQL\_PYTHON\_UDF\_TEST][](name) <a name="module_YQL_PYTHON_UDF_TEST"></a>
The Python test for Python YQL UDF (Python User Defined Function for YQL). The code should be a proper YQL\_PYTHON\_UDF.

This module will basically build itself as UDF and run as test using yql/tools/run\_python\_udf/run\_python\_udf tool.

Documentation: https://yql.yandex-team.ru/docs/yt/udf/python/

@example: https://a.yandex-team.ru/arc/trunk/arcadia/yql/udfs/test/simple/ya.make

@see: [YQL\_PYTHON\_UDF()](#module\_YQL\_PYTHON\_UDF)

###### Module [YQL\_UDF\_MODULE][](name) <a name="module_YQL_UDF_MODULE"></a>
The extension module for YQL with C++ UDF (User Defined Function YQL)

https://yql.yandex-team.ru/docs/yt/udf/cpp/

###### Module [YQL\_UDF\_TEST][]([name]) <a name="module_YQL_UDF_TEST"></a>
The module to test YQL C++ UDF.

Documentation: https://yql.yandex-team.ru/docs/yt/libraries/testing/
Documentation about the Arcadia test system: https://wiki.yandex-team.ru/yatool/test/

###### Module [YT\_UNITTEST][]([name]) <a name="module_YT_UNITTEST"></a>
YT Unit test module based on mapreduce/yt/library/utlib

###### Module [Y\_BENCHMARK][]([benchmarkname]) <a name="module_Y_BENCHMARK"></a>
Benchmark test based on the library/cpp/testing/benchmark.

For more details see: https://wiki.yandex-team.ru/yatool/test/#zapuskbenchmark

###### Module [\_BARE\_UNIT][]  _# internal_ <a name="module__BARE_UNIT"></a>
The base of all modules describing default bare minimum for all modules.
To avoid surprises, all buildable modules are better to be inherited from it or its descendants.

###### Module [\_BASE\_PROGRAM][]  _# internal_ <a name="module__BASE_PROGRAM"></a>
The base of all programs. It adds dependencies to make final artefact complete and runnable.

###### Module \_BASE\_PY\_PROGRAM _#internal_ <a name="module__BASE_PY3_PROGRAM"></a>
The base module for all Python 3.x binary programs. Adds linking logic, relevant module properties and
dependency on Python 3.x interpreter. Also adds import tests on all sources including libraries.
Links all Python 3.x libraries and Python 3.x interpreter into itself to form regular executable.
This only compatible with PYTHON3-tagged modules and selects those from multimodules

Documentation: https://wiki.yandex-team.ru/devtools/commandsandvars/py\_srcs/

###### Module [\_BASE\_PYTEST][]  _# internal_ <a name="module__BASE_PYTEST"></a>
Base logic of Python 2.x py.test modules: common module properties and dependencies.

###### Module [\_BASE\_PY\_PROGRAM][] _#internal_ <a name="module__BASE_PY_PROGRAM"></a>
The base module for all Python 2.x binary programs. Adds linking logic, relevant module properties and
dependency on Python 2.x interpreter. Also adds import tests on all sources including PEERDIR'ed libraries.
Links all Python 2.x libraries and Python 2.x interpreter into itself to form regular executable.
This only compatible with PYTHON2-tagged modules and selects those from multimodules.

Documentation: https://wiki.yandex-team.ru/devtools/commandsandvars/py\_srcs/

###### Module [\_BASE\_UNIT][]  _# internal_ <a name="module__BASE_UNIT"></a>
The base of all LIBRARY/PROGRAM modules describing common logic for all modules.
To avoid surprises, all buildable modules are better to be inherited from it or its descendants.

###### Module [\_BASE\_UNITTEST][]  _# internal_ <a name="module__BASE_UNITTEST"></a>
Module with base logic for all unit-test modules: it makes code runnable as unit-test by Arcadia testing machinery.

###### Module [\_COMPILABLE\_JAR\_BASE][] : \_JAR\_BASE _#internal_ <a name="module__COMPILABLE_JAR_BASE"></a>
Not documented yet.

###### Module [\_DLL\_COMPATIBLE\_LIBRARY][] _# internal_ <a name="module__DLL_COMPATIBLE_LIBRARY"></a>
Base module to place DLLs into multimodules back to back with libraries.
In order to function properly all modules in multimodule shall have the
same set of arguments. So this module is just library that accepts but
ignores all DLL arguments.

###### Module [\_DOCS\_BARE\_UNIT][] _#internal_ <a name="module__DOCS_BARE_UNIT"></a>
This module is intended for internal use only. Common parts for DOCS and MKDOCS multimodules
should be defined here.

###### Module [\_DOCS\_BASE\_UNIT][] _#internal_ <a name="module__DOCS_BASE_UNIT"></a>
This module is intended for internal use only. Common parts for submodules of DOCS multimodule
should be defined here.

###### Module [\_GO\_BASE\_UNIT][] _# internal_ <a name="module__GO_BASE_UNIT"></a>
The base module of all golang modules. Defines common properties, dependencies and rules for go build.

###### Module [\_GO\_DLL\_BASE\_UNIT][]: GO\_PROGRAM _#internal_ <a name="module__GO_DLL_BASE_UNIT"></a>
Not documented yet.

###### Module [\_JAR\_BASE][]: \_BARE\_UNIT _#internal_ <a name="module__JAR_BASE"></a>
Not documented yet.

###### Module [\_JAR\_RUNNABLE][]: \_COMPILABLE\_JAR\_BASE _#internal_ <a name="module__JAR_RUNNABLE"></a>
Not documented yet.

###### Module [\_JAR\_TEST][]: \_COMPILABLE\_JAR\_BASE _#internal_ <a name="module__JAR_TEST"></a>
Not documented yet.

###### Module [\_JAVA\_PLACEHOLDER][] _#internal_ <a name="module__JAVA_PLACEHOLDER"></a>
The base module for all Java modules. Defines common properties and dependencies.

###### Module [\_LIBRARY][] _# internal_ <a name="module__LIBRARY"></a>
Base module definition for all libraries.
Contains basic logic like module properties, default variable values etc.
All libraries similar to C++-libraries should be inherited from it.

###### Module [\_LINK\_UNIT][]  _# internal_ <a name="module__LINK_UNIT"></a>
The base of all linkable modules: programs, DLLs etc. Describes common linking logic.

###### Module [\_MKDOCS\_BASE\_UNIT][] _#internal_ <a name="module__MKDOCS_BASE_UNIT"></a>
This module is intended for internal use only. Common parts for submodules of MKDOCS multimodule
should be defined here.

###### Module [\_PROXY\_LIBRARY][]() _# internal_ <a name="module__PROXY_LIBRARY"></a>
The use of this module is strictly prohibited!!!

###### Module [\_PY2\_PROGRAM][]: \_BASE\_PY\_PROGRAM _#internal_ <a name="module__PY2_PROGRAM"></a>
Not documented yet.

###### Module [\_PY\_PACKAGE][]: UNION _#internal_ <a name="module__PY_PACKAGE"></a>
Not documented yet.

###### Module [\_TS\_BASE\_LIBRARY][] : \_TS\_BASE\_UNIT _#internal_ <a name="module__TS_BASE_LIBRARY"></a>
Not documented yet.

###### Module [\_TS\_BASE\_UNIT][]: \_BASE\_UNIT _#internal_ <a name="module__TS_BASE_UNIT"></a>
Not documented yet.

###### Module [\_YQL\_UDF\_PROGRAM\_BASE][]: SO\_PROGRAM _#internal_ <a name="module__YQL_UDF_PROGRAM_BASE"></a>
Not documented yet.

## Macros <a name="macros"></a>

###### Macro [AARS][](Aars...) <a name="macro_AARS"></a>
This macro is strictly prohibited to use outside of mapsmobi project

###### Macro [AAR\_AARS][](aars...) _# internal_ <a name="macro_AAR_AARS"></a>
Not documented yet.

###### Macro [AAR\_AIDL\_SRCS][](dir filenames...) _# internal_ <a name="macro_AAR_AIDL_SRCS"></a>
Not documented yet.

###### Macro [AAR\_ASSETS\_SRCS][](dir filenames...) _# internal_ <a name="macro_AAR_ASSETS_SRCS"></a>
Not documented yet.

###### Macro [AAR\_BUNDLES][](filenames...) _# internal_ <a name="macro_AAR_BUNDLES"></a>
Not documented yet.

###### Macro [AAR\_COMPILE\_ONLY\_AARS][](compile\_only\_aars...) _# internal_ <a name="macro_AAR_COMPILE_ONLY_AARS"></a>
Not documented yet.

###### Macro [AAR\_GRADLE\_SCRIPT\_GENERATOR][](python\_script) <a name="macro_AAR_GRADLE_SCRIPT_GENERATOR"></a>
Not documented yet.

###### Macro [AAR\_JAVA\_SRCS][](dir filenames...) _# internal_ <a name="macro_AAR_JAVA_SRCS"></a>
Not documented yet.

###### Macro [AAR\_JNI\_LIBS][](dir filenames...) _# internal_ <a name="macro_AAR_JNI_LIBS"></a>
Not documented yet.

###### Macro [AAR\_LOCAL\_MAVEN\_REPO][](repo...) <a name="macro_AAR_LOCAL_MAVEN_REPO"></a>
Not documented yet.

###### Macro [AAR\_MANIFEST][](filename) _# internal_ <a name="macro_AAR_MANIFEST"></a>
Not documented yet.

###### Macro [AAR\_PROGUARD\_RULES][](filename) _# internal_ <a name="macro_AAR_PROGUARD_RULES"></a>
Not documented yet.

###### Macro [AAR\_RES\_SRCS][](dir filenames...) _# internal_ <a name="macro_AAR_RES_SRCS"></a>
Not documented yet.

###### Macro [ACCELEO][](XSD{input}[], MTL{input}[], MTL\_ROOT="${MODDIR}", LANG{input}[], OUT{output}[], OUT\_NOAUTO{output}[], OUTPUT\_INCLUDES[], DEBUG?"stdout2stderr":"stderr2stdout") <a name="macro_ACCELEO"></a>
Not documented yet.

###### Macro [ADDINCL][]([FOR <lang>][GLOBAL dir]\* dirlist)  _# builtin_ <a name="macro_ADDINCL"></a>
The macro adds the directories to include/import search path to compilation flags of the current project.
By default settings apply to C/C++ compilation namely sets -I<library path> flag, use FOR argument to change target command.
@params:
`FOR <lang>` - adds inclues/import serach path for othe language. E.g. `FOR proto` adds import search path for .proto files processing.
`GLOBAL` - extends the search for headers (-I) on the dependent projects.

###### Macro [ADDINCLSELF][]() <a name="macro_ADDINCLSELF"></a>
The macro adds the -I<project source path> flag to the source compilation flags of the current project.

###### Macro [ADD\_CHECK][] <a name="macro_ADD_CHECK"></a>
Not documented yet.

###### Macro [ADD\_CHECK\_PY\_IMPORTS][] <a name="macro_ADD_CHECK_PY_IMPORTS"></a>
Not documented yet.

###### Macro [ADD\_CLANG\_TIDY][]() <a name="macro_ADD_CLANG_TIDY"></a>
Not documented yet.

###### Macro [ADD\_COMPILABLE\_TRANSLATE][](Dict Name Options...) <a name="macro_ADD_COMPILABLE_TRANSLATE"></a>
Generate translation dictionary code to transdict.LOWER(Name).cpp that will than be compiled into library

###### Macro [ADD\_COMPILABLE\_TRANSLIT][](TranslitTable NGrams Name Options...) <a name="macro_ADD_COMPILABLE_TRANSLIT"></a>
Generate transliteration dictionary code
This will emit both translit, untranslit and ngrams table codes those will be than further compiled into library

###### Macro [ADD\_DLLS\_TO\_JAR][]() <a name="macro_ADD_DLLS_TO_JAR"></a>
Not documented yet.

###### Macro [ADD\_PERL\_MODULE][](Dir ModuleName) <a name="macro_ADD_PERL_MODULE"></a>
Add dependency on specified Perl module to the library

###### Macro [ADD\_PYTEST\_BIN][] <a name="macro_ADD_PYTEST_BIN"></a>
Not documented yet.

###### Macro [ADD\_PYTEST\_SCRIPT][] <a name="macro_ADD_PYTEST_SCRIPT"></a>
Not documented yet.

###### Macro [ADD\_YTEST][] <a name="macro_ADD_YTEST"></a>
Not documented yet.

###### Macro [ALLOCATOR][](Alloc)  _# Default: LF_ <a name="macro_ALLOCATOR"></a>
Set memory allocator implementation for the PROGRAM()/DLL() module.
This may only be specified for programs and dlls, use in other modules leads to configuration errors.

Available allocators are: "LF", "LF\_YT", "LF\_DBG", "YT", "J", "B", "BM", "C", "TCMALLOC", "GOOGLE", "LOCKLESS", "SYSTEM", "FAKE", "MIM", "HU".
  - LF - lfalloc (https://a.yandex-team.ru/arc/trunk/arcadia/library/cpp/lfalloc)
  - LF\_YT -  Allocator selection for YT (https://a.yandex-team.ru/arc/trunk/arcadia/library/cpp/lfalloc/yt/ya.make)
  - LF\_DBG -  Debug allocator selection (https://a.yandex-team.ru/arc/trunk/arcadia/library/cpp/lfalloc/dbg/ya.make)
  - YT - The YTAlloc allocator (https://a.yandex-team.ru/arc/trunk/arcadia/library/cpp/ytalloc/impl/ya.make)
  - J - The JEMalloc allocator (https://a.yandex-team.ru/arc/trunk/arcadia/library/malloc/jemalloc)
  - B - The balloc allocator named Pyotr Popov and Anton Samokhvalov
      - Discussion: https://ironpeter.at.yandex-team.ru/replies.xml?item\_no=126
      - Code: https://a.yandex-team.ru/arc/trunk/arcadia/library/cpp/balloc
  - BM - The balloc for market (agri@ commits from july 2018 till November 2018 saved)
  - C - Like B, but can be disabled for each thread to LF or SYSTEM one (B can be disabled only to SYSTEM)
  - MIM -  Microsoft's mimalloc (actual version) (https://a.yandex-team.ru/arc/trunk/arcadia/library/malloc/mimalloc)
  - TCMALLOC -  Google TCMalloc (actual version) (https://a.yandex-team.ru/arc/trunk/arcadia/library/malloc/tcmalloc)
  - GOOGLE -  Google TCMalloc (https://a.yandex-team.ru/arc/trunk/arcadia/library/malloc/galloc)
  - LOCKLESS - Allocator based upon lockless queues (https://a.yandex-team.ru/arc/trunk/arcadia/library/malloc/lockless)
  - SYSTEM - Use target system allocator
  - FAKE - Don't link with any allocator

More about allocators in Arcadia: https://wiki.yandex-team.ru/arcadia/allocators/

###### Macro [ALL\_PYTEST\_SRCS][]([RECURSIVE] [Dirs...]) <a name="macro_ALL_PYTEST_SRCS"></a>
Puts all .py-files from given Dirs (relative to projects') into TEST\_SRCS of the current module.
If Dirs is omitted project directory is used

`RECURSIVE` makes lookup recursive with respect to Dirs
`ONLY\_TEST\_FILES` includes only files `test\_\*.py` and `\*\_test.py`, others are normally subject to `PY\_SRCS`

Note: Only one such macro per module is allowed
Note: Macro is designed to reject any ya.make files in Dirs except current one

@see [TEST\_SRCS()](#macro\_TEST\_SRCS)

###### Macro [ALL\_PY\_SRCS][]([RECURSIVE] [NO\_TEST\_FILES] { | TOP\_LEVEL | NAMESPACE ns} [Dirs...]) <a name="macro_ALL_PY_SRCS"></a>
Puts all .py-files from given Dirs (relative to projects') into PY\_SRCS of the current module.
If Dirs is ommitted project directory is used

`RECURSIVE` makes lookup recursive with resprect to Dirs
`NO\_TEST\_FILES` excludes files `test\_\*.py` and `\*\_test.py` those are normally subject to `TEST\_SRCS`
`TOP\_LEVEL` and `NAMESPACE` are forwarded to `PY\_SRCS`

Note: Only one such macro per module is allowed
Note: Macro is designed to reject any ya.make files in Dirs except current one

@see [PY\_SRCS()](#macro\_PY\_SRCS)

###### Macro [ALL\_RESOURCE\_FILES][](Ext [PREFIX {prefix}] [STRIP {strip}] Dirs...) <a name="macro_ALL_RESOURCE_FILES"></a>
This macro collects all files with extension `Ext` and
Passes them to `RESOURCE\_FILES` macro as relative to current directory

`PREFIX` and `STRIP` have the same meaning as in `ROURCES\_FILES`, both are applied over moddir-relative paths

Note: This macro can be used multiple times per ya.make, but only once for each Ext value
Note: Wildcards are not allowed neither as Ext nor in Dirs

###### Macro [ALL\_SRCS][]([GLOBAL] filenames...) <a name="macro_ALL_SRCS"></a>
Make all source files listed as GLOBAL or not depending on the keyword GLOBAL
Call to ALL\_SRCS macro is equivalent to call to GLOBAL\_SRCS macro when GLOBAL keyword is specified
as the first argument and is equivalent to call to SRCS macro otherwise.

@example:

    LIBRARY()
        SET(MAKE_IT_GLOBAL GLOBAL)
        ALL_SRCS(${MAKE_IT_GLOBAL} foo.cpp bar.cpp)
    END()

@see: [GLOBAL\_SRCS()](#macro\_GLOBAL\_SRCS), [SRCS()](#macro\_SRCS)

###### Macro [ANNOTATION\_PROCESSOR][](processors...) <a name="macro_ANNOTATION_PROCESSOR"></a>
The macro is in development.
Used to specify annotation processors to build JAVA\_PROGRAM() and JAVA\_LIBRARY().

###### Macro [APPHOST][]() <a name="macro_APPHOST"></a>
Emit APPHOST service code for all .proto files in a PROTO\_LIBRARY.
This works only for C++ and Java at the moment.

###### Macro [ARCHIVE][](archive\_name [DONT\_COMPRESS] files...) <a name="macro_ARCHIVE"></a>
Add arbitrary data to a modules. Unlike RESOURCE macro the result should be futher processed by othet macros in the module.

Example: https://wiki.yandex-team.ru/yatool/howtowriteyamakefiles/#a1ispolzujjtekomanduarchive

###### Macro [ARCHIVE\_ASM][](NAME archive\_name files...) <a name="macro_ARCHIVE_ASM"></a>
Similar to the macro ARCHIVE, but:
1. works faster and it is better to use for large files.
2. Different syntax (see examples in codesearch or users/pg/tests/archive\_test)

###### Macro [ARCHIVE\_BY\_KEYS][](archive\_name key [DONT\_COMPRESS] files...) <a name="macro_ARCHIVE_BY_KEYS"></a>
Add arbitrary data to a module be accessible by specified key.
Unlike RESOURCE macro the result should be futher processed by othet macros in the module.

Example: https://wiki.yandex-team.ru/yatool/howtowriteyamakefiles/#a1ispolzujjtekomanduarchive

###### Macro [ASM\_PREINCLUDE][](AsmFiles...) <a name="macro_ASM_PREINCLUDE"></a>
Supply additional .asm files to all assembler calls within a module

###### Macro [ASSERT][] <a name="macro_ASSERT"></a>
Not documented yet.

###### Macro [BASE\_CODEGEN][](tool\_path prefix) <a name="macro_BASE_CODEGEN"></a>
Generator ${prefix}.cpp + ${prefix}.h files based on ${prefix}.in.

###### Macro [BISON\_FLAGS][](<flags>) <a name="macro_BISON_FLAGS"></a>
Set flags for Bison tool invocations.

###### Macro [BISON\_GEN\_C][]() <a name="macro_BISON_GEN_C"></a>
Generate C from Bison grammar. The C++ is generated by default.

###### Macro [BISON\_GEN\_CPP][]() <a name="macro_BISON_GEN_CPP"></a>
Generate C++ from Bison grammar. This is current default.

###### Macro [BISON\_HEADER][](<header\_suffix>) <a name="macro_BISON_HEADER"></a>
Use SUFF (including extension) to name Bison defines header file. The default is just `.h`.

###### Macro [BISON\_NO\_HEADER][]() <a name="macro_BISON_NO_HEADER"></a>
Don't emit Bison defines header file.

###### Macro [BPF][](Input Output Opts...) <a name="macro_BPF"></a>
Emit eBPF bytecode from .c file.
Note: Output name is used as is, no extension added.

###### Macro [BPF\_STATIC][](Input Output Opts...) <a name="macro_BPF_STATIC"></a>
Emit eBPF bytecode from .c file.
Note: Output name is used as is, no extension added.

###### Macro [BUILDWITH\_CYTHON\_C][](Src Options...) <a name="macro_BUILDWITH_CYTHON_C"></a>
Generates .c file from .pyx.

###### Macro [BUILDWITH\_CYTHON\_CPP][](Src Options...) <a name="macro_BUILDWITH_CYTHON_CPP"></a>
Generates .cpp file from .pyx.

###### Macro [BUILDWITH\_RAGEL6][](Src Options...) <a name="macro_BUILDWITH_RAGEL6"></a>
Compile .rl file using Ragel6.

###### Macro [BUILD\_CATBOOST][](cbmodel cbname) <a name="macro_BUILD_CATBOOST"></a>
Generate catboost model and access code.
cbmodel - CatBoost model file name (\*.cmb).
cbname - name for a variable (of NCatboostCalcer::TCatboostCalcer type) to be available in CPP code.
CatBoost specific macro.

###### Macro [BUILD\_MN][]([CHECK] [PTR] [MULTI] mninfo mnname) _# matrixnet_ <a name="macro_BUILD_MN"></a>
Generate MatrixNet data and access code using single command.
Alternative macro BUILD\_MNS() works faster and better for large files.

###### Macro [BUILD\_MNS][]([CHECK] NAME listname mninfos...) _# matrixnet_ <a name="macro_BUILD_MNS"></a>
Generate MatrixNet data and access code using separate commands for support code, interface and data.
Faster version of BUILD\_MN() macro for large files.

###### Macro [BUILD\_ONLY\_IF][](variables)  _# builtin_ <a name="macro_BUILD_ONLY_IF"></a>
Print warning if all variables are false. For example, BUILD\_ONLY\_IF(LINUX WIN32)

###### Macro [BUILD\_YDL\_DESC][](Input Symbol Output) <a name="macro_BUILD_YDL_DESC"></a>
Generate a descriptor for a Symbol located in a ydl module Input, and put it to the file Output.

@example:

    PACKAGE()
        BUILD_YDL_DESC(../types.ydl Event Event.ydld)
    END()

This will parse file ../types.ydl, generate a descriptor for a symbol Event defined in the said file, and put the descriptor to the Event.ydld.

###### Macro [BUNDLE][](<Dir [NAME Name]>...) <a name="macro_BUNDLE"></a>
Brings build artefact from module Dir under optional Name to the current module (e.g. UNION)
If NAME is not specified, the name of the Dir's build artefact will be preserved
It makes little sense to specify BUNDLE on non-final targets and so this may stop working without prior notice.
Bundle on multimodule will select final target among multimodule variants and will fail if there are none or more than one.

###### Macro [BUNDLE\_AIDL\_SRCS][](dirname filenames...) _# internal_ <a name="macro_BUNDLE_AIDL_SRCS"></a>
Not documented yet.

###### Macro [BUNDLE\_ASSETS\_SRCS][](dirname filenames...) _# internal_ <a name="macro_BUNDLE_ASSETS_SRCS"></a>
Not documented yet.

###### Macro [BUNDLE\_EXTRA\_INPUTS][](filenames...) _# internal_ <a name="macro_BUNDLE_EXTRA_INPUTS"></a>
Not documented yet.

###### Macro [BUNDLE\_JAVA\_SRCS][](dirname filenames...) _# internal_ <a name="macro_BUNDLE_JAVA_SRCS"></a>
Not documented yet.

###### Macro [BUNDLE\_RES\_SRCS][](dirname filenames...) _# internal_ <a name="macro_BUNDLE_RES_SRCS"></a>
Not documented yet.

###### Macro $[CFG\_VARS][] _# internal_ <a name="macro_CFG_VARS"></a>
Mark commands that embed Configuration variables into files

###### Macro [CFLAGS][]([GLOBAL compiler\_flag]\* compiler\_flags) <a name="macro_CFLAGS"></a>
Add the specified flags to the compilation command of C and C++ files.
@params: GLOBAL - Propagates these flags to dependent projects
Note: remember about the incompatibility flags for clang and cl (to set flags specifically for cl.exe use MSVC\_FLAGS).

###### Macro [CGO\_CFLAGS][](Flags...) <a name="macro_CGO_CFLAGS"></a>
Compiler flags specific to CGO compilation

###### Macro [CGO\_LDFLAGS][](Files...) <a name="macro_CGO_LDFLAGS"></a>
Linker flags specific to CGO linking

###### Macro [CGO\_SRCS][](Files...) <a name="macro_CGO_SRCS"></a>
.go sources to be built with CGO

###### Macro [CHECK\_ALLOWED\_PATH][] <a name="macro_CHECK_ALLOWED_PATH"></a>
Not documented yet.

###### Macro [CHECK\_CONFIG\_H][](<conf\_header>) _# internal_ <a name="macro_CHECK_CONFIG_H"></a>
This internal macro adds checking code for configuration header in external (contrib) library.
The check is needed to avoid conflicts on certain types and functions available in arcadia.

@see https://a.yandex-team.ru/arc/trunk/arcadia/build/scripts/check\_config\_h.py for exact details

###### Macro [CHECK\_CONTRIB\_CREDITS][] <a name="macro_CHECK_CONTRIB_CREDITS"></a>
Not documented yet.

###### Macro [CHECK\_DEPENDENT\_DIRS][](DENY|ALLOW\_ONLY ([ALL|PEERDIRS|GLOB] dir)...) <a name="macro_CHECK_DEPENDENT_DIRS"></a>
Specify project transitive dependencies constraints.

@params:
 1. DENY: current module can not depend on module from any specified directory neither directly nor transitively.
 2. ALLOW\_ONLY: current module can not depend on module from a dir not specified in the directory list neither directly nor transitively.
 3. ALL: directory constraints following after this modifier are applied to both transitive PEERDIR dependencies and tool dependencies.
 4. PEERDIRS: directory constraints following after this modifier are applied to transitive PEERDIR dependencies only.
 5. GLOB: next directory constraint is an ANT glob pattern.
 6. EXCEPT: next constraint is an exception for the rest of other rules.

Directory constraints added before either ALL or PEERDIRS modifier is used are treated as ALL directory constraints.

Note: Can be used multiple times on the same module all specified constraints will be checked.
All macro invocation for the same module must use same constraints type (DENY or ALLOW\_ONLY)

###### Macro [CHECK\_JAVA\_DEPS][](<yes|no>) <a name="macro_CHECK_JAVA_DEPS"></a>
Check for different classes with duplicate name in classpath.

Documentation: https://wiki.yandex-team.ru/yatool/test/

###### Macro [CLANG\_EMIT\_AST\_CXX][](Input Output Opts...) <a name="macro_CLANG_EMIT_AST_CXX"></a>
Emit Clang AST from .cpp file. CXXFLAGS and LLVM\_OPTS are passed in, while CFLAGS and C\_FLAGS\_PLATFORM are not.
Note: Output name is used as is, no extension added.

###### Macro [CLEAN\_TEXTREL][]() <a name="macro_CLEAN_TEXTREL"></a>
Not documented yet.

###### Macro [CMAKE\_EXPORTED\_TARGET\_NAME][](Name) <a name="macro_CMAKE_EXPORTED_TARGET_NAME"></a>
Forces to use the name given as cmake target name without changing the name of output artefact.
This macro should be used to resolve target name conflicts in  exported cmake project when
changing module name is not applicable. For example both CUDA and non-CUDA py modules for
catboost should have same name lib\_catboost.so and both of them are defined as PY\_ANY\_MODULE(\_catboost).
adding CMAKE\_EXPORTED\_TARGET\_NAME(\_catboost\_non\_cuda) to the non CUDA module ya.make file
changes exported cmake target name but preserve generated artefact file name.

###### Macro [COLLECT\_FRONTEND\_FILES][](Varname, Dir) <a name="macro_COLLECT_FRONTEND_FILES"></a>
Recursively collect files with typical frontend extensions from Dir and save the result into variable Varname

###### Macro [COLLECT\_JINJA\_TEMPLATES][](varname path) <a name="macro_COLLECT_JINJA_TEMPLATES"></a>
This macro collects all jinja and yaml files in the directory specified by second argument and
stores result in the variable with mane specified by first parameter.

###### Macro [COLLECT\_YDB\_API\_SPECS\_LEGACY][](VarName Paths...)  _#deprecated_ <a name="macro_COLLECT_YDB_API_SPECS_LEGACY"></a>
This macro is ugly hack for legacy YDB go API codegen, any other uses are prohibited

###### Macro [COMPILE\_C\_AS\_CXX][]() <a name="macro_COMPILE_C_AS_CXX"></a>
Compile .c files as .cpp ones within a module.

###### Macro [COMPILE\_LUA][](Src, [NAME <import\_name>]) <a name="macro_COMPILE_LUA"></a>
Compile LUA source file to object code using LUA 2.0
Optionally override import name which is by default reflects Src name

###### Macro [COMPILE\_LUA\_21][](Src, [NAME <import\_name>]) <a name="macro_COMPILE_LUA_21"></a>
Compile LUA source file to object code using LUA 2.1
Optionally override import name which is by default reflects Src name

###### Macro [COMPILE\_NLG][]([LOCALIZED\_NLG\_TRANSLATIONS\_JSON translations.json] Src...) <a name="macro_COMPILE_NLG"></a>
Generate and compile .nlg templates (Jinja2-based) and interface for megamind runtime.

Alice-specific macro

###### Macro [COMPILE\_SWIFT\_MODULE][](SRCS{input}[], BRIDGE\_HEADER{input}="", Flags...) <a name="macro_COMPILE_SWIFT_MODULE"></a>
Not documented yet.

###### Macro [CONFIGURE\_FILE][](from to) <a name="macro_CONFIGURE_FILE"></a>
Copy file with the replacement of configuration variables in form of @ANY\_CONF\_VAR@ with their values.
The values are collected during configure stage, while replacement itself happens during build stage.
Used implicitly for .in-files processing.

###### Macro [CONFTEST\_LOAD\_POLICY\_LOCAL][]() <a name="macro_CONFTEST_LOAD_POLICY_LOCAL"></a>
Loads conftest.py files in a way that pytest does it

###### Macro [CONLYFLAGS][]([GLOBAL compiler\_flag]\* compiler\_flags) <a name="macro_CONLYFLAGS"></a>
Add the specified flags to the compilation command of .c (but not .cpp) files.
@params: GLOBAL - Distributes these flags on dependent projects

###### Macro [COPY][] <a name="macro_COPY"></a>
Not documented yet.

###### Macro [COPY\_FILE][](File Destination [AUTO] [OUTPUT\_INCLUDES Deps...]) <a name="macro_COPY_FILE"></a>
Copy file to build root. It is possible to change both location and the name.

Parameters:
- File - Source file name.
- Destination - Output file name.
- AUTO - Consider copied file for further processing automatically.
- OUTPUT\_INCLUDES output\_includes... - Output file dependencies.
- INDUCED\_DEPS $VARs... - Dependencies for generated files. Unlike `OUTPUT\_INCLUDES` these may target files further in processing chain.
                          In order to do so VAR should be filled by PREPARE\_INDUCED\_DEPS macro, stating target files (by type)
                          and set of dependencies

The file will be just copied if AUTO boolean parameter is not specified. You should explicitly
mention it in SRCS under new name (or specify AUTO boolean parameter) for further processing.

###### Macro [COPY\_FILE\_WITH\_CONTEXT][](FILE DEST [AUTO] [OUTPUT\_INCLUDES DEPS...]) <a name="macro_COPY_FILE_WITH_CONTEXT"></a>
Copy file to build root the same way as it is done for COPY\_FILE, but also
propagates the context of the source file.

###### Macro [CPP\_ADDINCL][](Dirs...) <a name="macro_CPP_ADDINCL"></a>
Not documented yet.

###### Macro [CPP\_ENUMS\_SERIALIZATION][] <a name="macro_CPP_ENUMS_SERIALIZATION"></a>
Not documented yet.

###### Macro [CPP\_PROTO\_PLUGIN][](Name Tool Suf DEPS <Dependencies>) <a name="macro_CPP_PROTO_PLUGIN"></a>
Define protoc plugin for C++ with given Name that emits code into 1 extra output
using Tool. Extra dependencies are passed via DEPS.

###### Macro [CPP\_PROTO\_PLUGIN0][](Name Tool DEPS <Dependencies>) <a name="macro_CPP_PROTO_PLUGIN0"></a>
Define protoc plugin for C++ with given Name that emits code into regular outputs
using Tool. Extra dependencies are passed via DEPS.

###### Macro [CPP\_PROTO\_PLUGIN2][](Name Tool Suf1 Suf2 DEPS <Dependencies>) <a name="macro_CPP_PROTO_PLUGIN2"></a>
Define protoc plugin for C++ with given Name that emits code into 2 extra outputs
using Tool. Extra dependencies are passed via DEPS.

###### Macro [CREATE\_BUILDINFO\_FOR][](GenHdr) <a name="macro_CREATE_BUILDINFO_FOR"></a>
Creates header file to access some information about build specified via configuration variables.
Unlike CREATE\_SVNVERSION\_FOR() it doesn't take revion information from VCS, it uses revision and SandboxTaskId passed via -D options to ya make

###### Macro [CREATE\_INIT\_PY\_STRUCTURE][] <a name="macro_CREATE_INIT_PY_STRUCTURE"></a>
Not documented yet.

###### Macro [CREDITS\_DISCLAIMER][] <a name="macro_CREDITS_DISCLAIMER"></a>
Not documented yet.

###### Macro [CTEMPLATE\_VARNAMES][](File) <a name="macro_CTEMPLATE_VARNAMES"></a>
Generate File.varnames.h using contrib/libs/ctemplate/make\_tpl\_varnames\_h

Documentation: https://a.yandex-team.ru/arc/trunk/arcadia/contrib/libs/ctemplate/README.md

###### Macro [CUDA\_NVCC\_FLAGS][](compiler flags) <a name="macro_CUDA_NVCC_FLAGS"></a>
Add the specified flags to the compile line .cu-files.

###### Macro [CUSTOM\_LINK\_STEP\_SCRIPT][](name) <a name="macro_CUSTOM_LINK_STEP_SCRIPT"></a>
Specifies name of a script for custom link step. The scripts
should be placed in the build/scripts directory and are subject to
review by devtools@.

###### Macro [CXXFLAGS][](compiler\_flags) <a name="macro_CXXFLAGS"></a>
Add the specified flags to the compilation command of .cpp (but not .c) files.

###### Macro [DARWIN\_SIGNED\_RESOURCE][](Resource, Relpath) <a name="macro_DARWIN_SIGNED_RESOURCE"></a>
Not documented yet.

###### Macro [DARWIN\_STRINGS\_RESOURCE][](Resource, Relpath) <a name="macro_DARWIN_STRINGS_RESOURCE"></a>
Not documented yet.

###### Macro [DATA][]([path...]) <a name="macro_DATA"></a>
Specifies the path to the data necessary test.
Valid values are: arcadia/<path> , arcadia\_tests\_data/<path> and sbr://<resource\_id>.
In the latter case resource will be brought to the working directory of the test before it is started

Used only inside TEST modules.

Documentation: https://wiki.yandex-team.ru/yatool/test/#dannyeizrepozitorija

###### Macro [DEB\_VERSION][](File) <a name="macro_DEB_VERSION"></a>
Creates a header file DebianVersion.h define the DEBIAN\_VERSION taken from the File.

###### Macro [DECIMAL\_MD5\_LOWER\_32\_BITS][](<fileName> [FUNCNAME funcName] [inputs...]) <a name="macro_DECIMAL_MD5_LOWER_32_BITS"></a>
Generates .cpp file <fileName> with one defined function 'const char\* <funcName>() { return "<calculated\_md5\_hash>"; }'.
<calculated\_md5\_hash> will be md5 hash for all inputs passed to this macro.

###### Macro [DECLARE\_EXTERNAL\_HOST\_RESOURCES\_BUNDLE][](name sbr:id FOR platform1 sbr:id FOR platform2...)  _#builtin_ <a name="macro_DECLARE_EXTERNAL_HOST_RESOURCES_BUNDLE"></a>
Associate name with sbr-id on platform.

Ask devtools@yandex-team.ru if you need more information

###### Macro [DECLARE\_EXTERNAL\_HOST\_RESOURCES\_BUNDLE\_BY\_JSON][](VarName, FileName [, FriendlyResourceName]) <a name="macro_DECLARE_EXTERNAL_HOST_RESOURCES_BUNDLE_BY_JSON"></a>
Associate 'Name' with a platform to resource uri mapping
File 'FileName' contains json with a 'canonized platform -> resource uri' mapping.
'FriendlyResourceName', if specified, is used in configuration error messages instead of VarName.
The mapping file format see in SET\_RESOURCE\_URI\_FROM\_JSON description.

###### Macro [DECLARE\_EXTERNAL\_HOST\_RESOURCES\_PACK][](RESOURCE\_NAME name sbr:id FOR platform1 sbr:id FOR platform2... RESOURCE\_NAME name1 sbr:id1 FOR platform1...)  _#builtin_ <a name="macro_DECLARE_EXTERNAL_HOST_RESOURCES_PACK"></a>
Associate name with sbr-id on platform.

Ask devtools@yandex-team.ru if you need more information

###### Macro [DECLARE\_EXTERNAL\_RESOURCE][](name sbr:id name1 sbr:id1...)  _#builtin_ <a name="macro_DECLARE_EXTERNAL_RESOURCE"></a>
Associate name with sbr-id.

Ask devtools@yandex-team.ru if you need more information

###### Macro [DECLARE\_EXTERNAL\_RESOURCE\_BY\_JSON][](VarName, FileName [, FriendlyResourceName]) <a name="macro_DECLARE_EXTERNAL_RESOURCE_BY_JSON"></a>
Associate 'Name' with a resource for the current target platform
File 'FileName' contains json with a 'canonized platform -> resource uri' mapping.
'FriendlyResourceName', if specified, is used in configuration error messages instead of VarName.
The mapping file format see in SET\_RESOURCE\_URI\_FROM\_JSON description.

###### Macro [DEFAULT][](varname value)  _#builtin_ <a name="macro_DEFAULT"></a>
Sets varname to value if value is not set yet

###### Macro [DEPENDENCY\_MANAGEMENT][](path/to/lib1 path/to/lib2 ...) <a name="macro_DEPENDENCY_MANAGEMENT"></a>
Lock version of the library from the contrib/java at some point, so that all unversioned PEERDIRs to this library refer to the specified version.

For example, if the module has PEERDIR (contrib/java/junit/junit), and
  1. specifies DEPENDENCY\_MANAGEMENT(contrib/java/junit/junit/4.12),
     the PEERDIR is automatically replaced by contrib/java/junit/junit/4.12;
  2. doesn't specify DEPENDENCY\_MANAGEMENT, PEERDIR automatically replaced
     with the default from contrib/java/junit/junit/ya.make.
     These defaults are always there and are supported by maven-import, which puts
     there the maximum version available in contrib/java.

The property is transitive. That is, if module A PEERDIRs module B, and B has PEERDIR(contrib/java/junit/junit), and this junit was replaced by junit-4.12, then junit-4.12 will come to A through B.

If some module has both DEPENDENCY\_MANAGEMENT(contrib/java/junit/junit/4.12) and PERDIR(contrib/java/junit/junit/4.11), the PEERDIR wins.

Documentation: https://wiki.yandex-team.ru/yatool/java/

###### Macro [DEPENDS][](path1 [path2...]) _# builtin_ <a name="macro_DEPENDS"></a>
Buildable targets that should be brought to the test run. This dependency isonly used when tests run is requested. It will build the specified modules andbring them to the working directory of the test (in their Arcadia paths). Itis reasonable to specify only final targets her (like programs, DLLs orpackages). DEPENDS to UNION is the only exception: UNIONs aretransitively closed at DEPENDS bringing all dependencies to the test.

DEPENDS on multimodule will select and bring single final target. If more noneor more than one final target available in multimodule DEPENDS to it willproduce configuration error.

###### Macro [DIRECT\_DEPS\_ONLY][] <a name="macro_DIRECT_DEPS_ONLY"></a>
Add direct PEERDIR's only in java compile classpath

###### Macro [DISABLE][](varname)  _#builtin_ <a name="macro_DISABLE"></a>
Sets varname to 'no'

###### Macro [DISABLE\_DATA\_VALIDATION][]() <a name="macro_DISABLE_DATA_VALIDATION"></a>
Not documented yet.

###### Macro [DLL\_FOR][](path/to/lib [libname] [major\_ver [minor\_ver]] [EXPORTS symlist\_file])  _#builtin_ <a name="macro_DLL_FOR"></a>
DLL module definition based on specified LIBRARY

###### Macro [DOCS\_CONFIG][](path) <a name="macro_DOCS_CONFIG"></a>
Specify path to config file for DOCS multimodule if it differs from default path.
If used for [MKDOCS](#multimodule\_MKDOCS) multimodule the default path is "%%project\_directory%%/mkdocs.yml".
If used for [DOCS](#multimodule\_DOCS) multimodule the default path is "%%project\_directory%%/.yfm".
Path must be either Arcadia root relative.

@see: [DOCS](#multimodule\_DOCS)

###### Macro [DOCS\_COPY\_FILES][](FROM src\_dir [NAMESPCE dst\_dir] files...) <a name="macro_DOCS_COPY_FILES"></a>
Copy files from src\_dir to $BINDIR/dst\_dir

###### Macro [DOCS\_DIR][](path) <a name="macro_DOCS_DIR"></a>
Specify directory with source .md files for DOCS multimodule if it differs from project directory.
Path must be Arcadia root relative.

@see: [DOCS](#multimodule\_DOCS)

###### Macro [DOCS\_INCLUDE\_SOURCES][](path...) <a name="macro_DOCS_INCLUDE_SOURCES"></a>
Specify a list of paths to source code files which will be used as text includes in a documentation project.
Paths must be Arcadia root relative.

@see: [DOCS](#multimodule\_DOCS)

###### Macro [DOCS\_VARS][](variable1=value1 variable2=value2 ...) <a name="macro_DOCS_VARS"></a>
Specify a set of default values of template variables for DOCS multimodule.
There must be no spaces around "=". Values will be treated as strings.

@see: [DOCS](#multimodule\_DOCS)

###### Macro [DUMPERF\_CODEGEN][](Prefix) <a name="macro_DUMPERF_CODEGEN"></a>
A special case BASE\_CODEGEN, in which the extsearch/images/robot/tools/dumperf/codegen tool is used

###### Macro [DYNAMIC\_DEPS][](Path...) _# internal, temporary_ <a name="macro_DYNAMIC_DEPS"></a>
Enlist paths to all DYNAMIC\_LIBRARY dependencies of the DYNAMIC\_LIBRARY
This it needed to transfer their outputs through the library to PROGRAM
or dependent DLL/DYNAMIC\_LIBRARY.

Note: this is temporary solution until support of `super-global` variables come
      which will enable transfer of some properties though final targets like DLLs.

###### Macro [DYNAMIC\_LIBRARY\_FROM][](Paths) <a name="macro_DYNAMIC_LIBRARY_FROM"></a>
Use specified libraries as sources of DLL

###### Macro IF(condition) .. [ELSE][]IF(other\_condition) .. ELSE() .. ENDIF()  _#builtin_ <a name="macro_ELSE"></a>
Apply macros if none of previous conditions hold

###### Macro IF(condition) .. [ELSEIF][](other\_condition) .. ELSE() .. ENDIF()  _#builtin_ <a name="macro_ELSEIF"></a>
Apply macros if other\_condition holds while none of previous conditions hold

###### Macro [EMBED\_JAVA\_VCS\_INFO][]() <a name="macro_EMBED_JAVA_VCS_INFO"></a>
Embed manifest with vcs info into `EXTERNAL\_JAVA\_LIBRARY`
By default this is disabled.

###### Macro [ENABLE][](varname)  _#builtin_ <a name="macro_ENABLE"></a>
Sets varname to 'yes'

###### Macro [ENABLE\_PREVIEW][]() <a name="macro_ENABLE_PREVIEW"></a>
Enable java preview features.

###### Macro [END][]()  _# builtin_ <a name="macro_END"></a>
The end of the module

###### Macro IF(condition) .. ELSEIF(other\_condition) .. ELSE() .. [ENDIF][]()  _#builtin_ <a name="macro_ENDIF"></a>
End of conditional construct

###### Macro [ENV][](key[=value]) <a name="macro_ENV"></a>
Sets env variable key to value (gets value from system env by default).

###### Macro [EXCLUDE][] <a name="macro_EXCLUDE"></a>
EXCLUDE(prefixes)

The macro is in development.
Specifies which libraries should be excluded from the classpath.

###### Macro [EXCLUDE\_TAGS][](tags...)  _# builtin_ <a name="macro_EXCLUDE_TAGS"></a>
Instantiate from multimodule all variants except ones with tags listed

###### Macro [EXPORTS\_SCRIPT][](exports\_file) <a name="macro_EXPORTS_SCRIPT"></a>
Specify exports script within PROGRAM, DLL and DLL-derived modules.
This accepts 2 kind of files: .exports with <lang symbol> pairs and JSON-line .symlist files.
The other option use EXPORTS parameter of the DLL module itself.

@see: [DLL](#module\_DLL)

###### Macro [EXPORT\_ALL\_DYNAMIC\_SYMBOLS][]() <a name="macro_EXPORT_ALL_DYNAMIC_SYMBOLS"></a>
Export all non-hidden symbols as dynamic when linking a PROGRAM.

###### Macro [EXPORT\_MAPKIT\_PROTO][]() _# internal deprecated_ <a name="macro_EXPORT_MAPKIT_PROTO"></a>
This macro is a temporary one and should be changed to EXPORT\_YMAPS\_PROTO
when transition of mapsmobi to arcadia is finished

###### Macro [EXPORT\_YMAPS\_PROTO][]() _# maps-specific_ <a name="macro_EXPORT_YMAPS_PROTO"></a>
Maps-specific .proto handling: IMPORT\_YMAPS\_PROTO() + maps protobuf namespace.

###### Macro [EXPOSE][](OutputsToExport...) <a name="macro_EXPOSE"></a>
Allows to mark outputs of macro command as unused in the current module but intended
to be used in modules consuming current via PEERDIR.

TODO(DEVTOOLS-9000) proper implementation needed

###### Macro [EXTERNAL\_JAR][] <a name="macro_EXTERNAL_JAR"></a>
Not documented yet.

###### Macro [EXTERNAL\_RESOURCE][](...)  _#builtin, deprecated_ <a name="macro_EXTERNAL_RESOURCE"></a>
Don't use this. Use RESOURCE\_LIBRARY or FROM\_SANDBOX instead

###### Macro [EXTRADIR][](...)  _#builtin, deprecated_ <a name="macro_EXTRADIR"></a>
Ignored

###### Macro [EXTRALIBS][](liblist)  _# builtin_ <a name="macro_EXTRALIBS"></a>
Add external dynamic libraries during program linkage stage

###### Macro [EXTRALIBS\_STATIC][](Libs...) <a name="macro_EXTRALIBS_STATIC"></a>
Add the specified external static libraries to the program link

###### Macro [FAT\_RESOURCE][] <a name="macro_FAT_RESOURCE"></a>
Not documented yet.

###### Macro [FBS\_NAMESPACE][](NAMESPACE, PATH...) <a name="macro_FBS_NAMESPACE"></a>
Not documented yet.

###### Macro [FBS\_TO\_PYSRC][](output\_base\_name fbs\_files...) _# internal_ <a name="macro_FBS_TO_PYSRC"></a>
Create a tar archive of .py files generated by flatc for Python. Output tar
archive will have .fbs.pysrc extension. This .fbs.pysrc extension is specially
processed when --add-flatbuf-result flag is specified on the command line
for 'ya make ...' (tar archive is extracted to output directory).

###### Macro [FILES][] <a name="macro_FILES"></a>
Not documented yet.

###### Macro [FLATC\_FLAGS][](flags...) <a name="macro_FLATC_FLAGS"></a>
Add flags to flatc command line

###### Macro [FLAT\_JOIN\_SRCS\_GLOBAL][](Out Src...) <a name="macro_FLAT_JOIN_SRCS_GLOBAL"></a>
Join set of sources into single file named Out and send it for further processing as if it were listed as SRCS(GLOBAL Out).
This macro places all files into single file, so will work with any sources.
You should specify file name with the extension as Out. Further processing will be done according to this extension.

###### Macro [FLEX\_FLAGS][](<flags>) <a name="macro_FLEX_FLAGS"></a>
Set flags for Lex tool (flex) invocations.

###### Macro [FLEX\_GEN\_C][]() <a name="macro_FLEX_GEN_C"></a>
Generate C from Lex grammar. The C++ is generated by default.

###### Macro [FLEX\_GEN\_CPP][]() <a name="macro_FLEX_GEN_CPP"></a>
Generate C++ from Lex grammar. This is current default.

###### Macro [FORK\_SUBTESTS][]() <a name="macro_FORK_SUBTESTS"></a>
Splits the test run in chunks on subtests.
The number of chunks can be overridden using the macro SPLIT\_FACTOR.

Allows to run tests in parallel. Supported in UNITTEST, JTEST/JUNIT5 and PY2TEST/PY3TEST modules.

Documentation about the system test: https://wiki.yandex-team.ru/yatool/test/

###### Macro [FORK\_TESTS][]() <a name="macro_FORK_TESTS"></a>
Splits a test run on chunks by test classes.
The number of chunks can be overridden using the macro SPLIT\_FACTOR.

Allows to run tests in parallel. Supported in UNITTEST, JTEST/JUNIT5 and PY2TEST/PY3TEST modules.

Documentation about the system test: https://wiki.yandex-team.ru/yatool/test/

###### Macro [FORK\_TEST\_FILES][]() <a name="macro_FORK_TEST_FILES"></a>
Only for PY2TEST and PY3TEST: splits a file executable with the tests on chunks in the files listed in TEST\_SRCS
Compatible with FORK\_(SUB)TESTS.

Documentation about the system test: https://wiki.yandex-team.ru/yatool/test/

###### Macro [FROM\_ARCHIVE][](Src [RENAME <resource files>] OUT\_[NOAUTO] <output files> [EXECUTABLE] [OUTPUT\_INCLUDES <include files>] [INDUCED\_DEPS $VARs...]) <a name="macro_FROM_ARCHIVE"></a>
Process file archive as [FROM\_SANDBOX()](#macro\_FROM\_SANDBOX).

###### Macro [FROM\_MDS][]([FILE] key [RENAME <resource files>] OUT\_[NOAUTO] <output files> [EXECUTABLE] [OUTPUT\_INCLUDES <include files>] [INDUCED\_DEPS $VARs...]) <a name="macro_FROM_MDS"></a>
Download resource from MDS with the specified key and process like [FROM\_SANDBOX()](#macro\_FROM\_SANDBOX).

###### Macro [FROM\_NPM][](NAME VERSION SKY\_ID INTEGRITY INTEGRITY\_ALGO TARBALL\_PATH) <a name="macro_FROM_NPM"></a>
Not documented yet.

###### Macro [FROM\_NPM\_LOCKFILES][](LOCKFILES...) _# internal_ <a name="macro_FROM_NPM_LOCKFILES"></a>
Defines lockfile list for `NPM\_CONTRIBS` module.

@see [NPM\_CONTRIBS()](#module\_NPM\_CONTRIBS)

###### Macro [FROM\_SANDBOX][]([FILE] resource\_id [AUTOUPDATED script] [RENAME <resource files>] OUT\_[NOAUTO] <output files> [EXECUTABLE] [OUTPUT\_INCLUDES <include files>] [INDUCED\_DEPS $VARs...]) <a name="macro_FROM_SANDBOX"></a>
Download the resource from the Sandbox, unpack (if not explicitly specified word FILE) and add OUT files to the build. EXECUTABLE makes them executable.
You may specify extra dependencies that output files bring using OUTPUT\_INCLUDES or INDUCED\_DEPS. The change of these may e.g. lead to recompilation of .cpp files extracted from resource.
If there is no default processing for OUT files or you need process them specially use OUT\_NOAUTO instead of OUT.

It is disallowed to specify directory as OUT/OUT\_NOAUTO since all outputs of commands shall be known to build system.

RENAME renames files to the corresponding OUT and OUT\_NOAUTO outputs:
FROM\_SANDBOX(resource\_id RENAME in\_file1 in\_file2 OUT out\_file1 out\_file2 out\_file3)
FROM\_SANDBOX(resource\_id RENAME in\_file1 OUT out\_file1 RENAME in\_file2 OUT out\_file2)
FROM\_SANDBOX(FILE resource\_id RENAME resource\_file OUT out\_name)

RENAME RESOURCE allows to rename the resource without specifying its file name.

OUTPUT\_INCLUDES output\_includes... - Includes of the output files that are needed to build them.
INDUCED\_DEPS $VARs... - Dependencies for generated files. Unlike `OUTPUT\_INCLUDES` these may target files further in processing chain.
                        In order to do so VAR should be filled by PREPARE\_INDUCED\_DEPS macro, stating target files (by type) and set of dependencies

If AUTOUPDATED is specified than macro will be regularly updated according to autoupdate script. The dedicated Sandbox task scans the arcadia and
changes resource\_ids in such macros if newer resource of specified type is available. Note that the task seeks AUTOUPDATED in specific position,
so you shall place it immediately after resource\_id.

###### Macro [FUZZ\_DICTS][](path1 [path2...]) <a name="macro_FUZZ_DICTS"></a>
Allows you to specify dictionaries, relative to the root of Arcadia, which will be used in Fuzzing.
Libfuzzer and AFL use a single syntax for dictionary descriptions.
Should only be used in FUZZ modules.

Documentation: https://wiki.yandex-team.ru/yatool/fuzzing/

###### Macro [FUZZ\_OPTS][](opt1 [Opt2...]) <a name="macro_FUZZ_OPTS"></a>
Overrides or adds options to the corpus mining and fuzzer run.
Currently supported only Libfuzzer, so you should use the options for it.
Should only be used in FUZZ modules.

@example:

    FUZZ_OPTS (
        -max_len=1024
        -rss_limit_mb=8192
    )

Documentation: https://wiki.yandex-team.ru/yatool/fuzzing/

###### Macro [GENERATED\_SRCS][](srcs... PARSE\_META\_FROM cpp\_srcs... [OUTPUT\_INCLUDES output\_includes...] [OPTIONS]) <a name="macro_GENERATED_SRCS"></a>
Generate sources using Jinja 2 template engine.

srcs... - list of text files which will be generated during build time by templates. Each template must be
    placed to the place in source tree where corresponding source file should be generated. Name of
    template must be "<name\_of\_src\_file>.markettemplate". For example if you want to generate file "example.cpp"
    then template should be named "example.cpp.markettemplate".
PARSE\_META\_FROM cpp\_srcs... - list of C++ source files (.cpp, .h) which will be parsed using clang library
    and metainformation extracted from the files will be made available for templates. Example of
    template code fragment using metainformation: {{ meta.objects["@N@std@S@string"].name }}
OUTPUT\_INCLUDES output\_includes... - in cases when build system parser fails to determine all headers
    which generated files include, you can specify additional headers here. In a normal situation this should
    not be needed and this feature could be removed in the future.
OPTIONS - additional options for code\_generator utility

Examples of templates can be found in directory market/tools/code\_generator/templates.
Metainformation does not contain entries for every object declared in C++ files specified in PARSE\_META\_FROM
parameter. To include some object into consideration you need to mark it by attribute. Attributes can
automatically add more attributes to dependent objects. This behavior depends on attribute definition.

More information will be available (eventually:) here: https://wiki.yandex-team.ru/Users/denisk/codegenerator/

###### Macro [GENERATE\_ENUM\_SERIALIZATION][](File.h) <a name="macro_GENERATE_ENUM_SERIALIZATION"></a>
Create serialization support for enumeration members defined in the header (String <-> Enum conversions) and compile it into the module.

Documentation: https://wiki.yandex-team.ru/yatool/HowToWriteYaMakeFiles/

###### Macro [GENERATE\_ENUM\_SERIALIZATION\_WITH\_HEADER][](File.h) <a name="macro_GENERATE_ENUM_SERIALIZATION_WITH_HEADER"></a>
Create serialization support for enumeration members defined in the header (String <-> Enum conversions) and compile it into the module
Provide access to serialization functions via generated header File\_serialized.h

Documentation: https://wiki.yandex-team.ru/yatool/HowToWriteYaMakeFiles/

###### Macro [GENERATE\_PY\_PROTOS][](ProtoFiles...) _# deprecated_ <a name="macro_GENERATE_PY_PROTOS"></a>
Generate python bindings for protobuf files.
Macro is obsolete and not recommended for use!

###### Macro [GENERATE\_SCRIPT][] <a name="macro_GENERATE_SCRIPT"></a>
heretic@ promised to make tutorial here
Don't forget
Feel free to remind

###### Macro [GEN\_SCHEEME2][](scheeme\_name from\_file dependent\_files...) <a name="macro_GEN_SCHEEME2"></a>
Generates a C++ description for structure(contains the field RecordSig) in the specified file (and connected).

1. ${scheeme\_name}.inc - the name of the generated file.
2. Use an environment variable - DATAWORK\_SCHEEME\_EXPORT\_FLAGS that allows to specify flags to tools/structparser

@example:

    SET(DATAWORK_SCHEEME_EXPORT_FLAGS --final_only -m "::")

all options are passed to structparser (in this example --final\_only - do not export heirs with public base that contains the required field,,- m "::" only from the root namespace)
sets in extra option

@example:

    SET(EXTRACT_STRUCT_INFO_FLAGS -f \"const static ui32 RecordSig\"
        -u \"RecordSig\" -n${scheeme_name}SchemeInfo ----gcc44_no_typename no_complex_overloaded_func_export
        ${DATAWORK_SCHEEME_EXPORT_FLAGS})

for compatibility with C++ compiler and the external environment.
See tools/structparser for more details.

###### Macro [GLOBAL\_SRCS][](filenames...) <a name="macro_GLOBAL_SRCS"></a>
Make all source files listed as GLOBAL.
Call to GLOBAL\_SRCS macro is equivalent to call to SRCS macro when each source file is marked with GLOBAL keyword.
Arcadia root relative or project dir relative paths are supported for filenames arguments. GLOBAL keyword is not
recognized for GLOBAL\_SRCS in contrast to SRCS macro.

@example:
Consider the file to ya.make:

    LIBRARY()
        GLOBAL_SRCS(foo.cpp bar.cpp)
    END()

@see: [SRCS()](#macro\_SRCS)

###### Macro [GOLANG\_VERSION][](Arg) <a name="macro_GOLANG_VERSION"></a>
Not documented yet.

###### Macro [GO\_ASM\_FLAGS][](flags) <a name="macro_GO_ASM_FLAGS"></a>
Add the specified flags to the go asm compile command line.

###### Macro [GO\_BENCH\_TIMEOUT][](x) <a name="macro_GO_BENCH_TIMEOUT"></a>
Sets timeout in seconds for 1 Benchmark in go benchmark suite

Documentation about the system test: https://wiki.yandex-team.ru/yatool/test/

###### Macro [GO\_CGO1\_FLAGS][](flags) <a name="macro_GO_CGO1_FLAGS"></a>
Add the specified flags to the go cgo compile command line.

###### Macro [GO\_CGO2\_FLAGS][](flags) <a name="macro_GO_CGO2_FLAGS"></a>
Add the specified flags to the go cgo compile command line.

###### Macro [GO\_COMPILE\_FLAGS][](flags) <a name="macro_GO_COMPILE_FLAGS"></a>
Add the specified flags to the go compile command line.

###### Macro [GO\_EMBED\_DIR][](DIR) <a name="macro_GO_EMBED_DIR"></a>
Define an embed directory DIR.

###### Macro [GO\_EMBED\_PATTERN][](PATTERN) <a name="macro_GO_EMBED_PATTERN"></a>
Define an embed pattern.

###### Macro [GO\_EMBED\_TEST\_DIR][](DIR) <a name="macro_GO_EMBED_TEST_DIR"></a>
Define an embed directory DIR for internal go tests.

###### Macro [GO\_EMBED\_XTEST\_DIR][](DIR) <a name="macro_GO_EMBED_XTEST_DIR"></a>
Define an embed directory DIR for external go tests.

###### Macro [GO\_FAKE\_OUTPUT][](go-src-files...) <a name="macro_GO_FAKE_OUTPUT"></a>
Not documented yet.

###### Macro [GO\_GRPC\_GATEWAY\_SRCS][]() <a name="macro_GO_GRPC_GATEWAY_SRCS"></a>
Use of grpc-gateway plugin (Supported for Go only).

###### Macro [GO\_GRPC\_GATEWAY\_SWAGGER\_SRCS][]() <a name="macro_GO_GRPC_GATEWAY_SWAGGER_SRCS"></a>
Use of grpc-gateway plugin w/ swagger emission (Supported for Go only).

###### Macro [GO\_LDFLAGS][](Flags...) <a name="macro_GO_LDFLAGS"></a>
Link flags for GO\_PROGRAM linking from .go sources

###### Macro [GO\_LINK\_FLAGS][](flags) <a name="macro_GO_LINK_FLAGS"></a>
Add the specified flags to the go link command line.

###### Macro [GO\_MOCKGEN\_FROM][](Path) <a name="macro_GO_MOCKGEN_FROM"></a>
Not documented yet.

###### Macro [GO\_MOCKGEN\_MOCKS][]() <a name="macro_GO_MOCKGEN_MOCKS"></a>
Not documented yet.

###### Macro [GO\_MOCKGEN\_REFLECT][]() <a name="macro_GO_MOCKGEN_REFLECT"></a>
Not documented yet.

###### Macro [GO\_MOCKGEN\_TYPES][](Types...) <a name="macro_GO_MOCKGEN_TYPES"></a>
Not documented yet.

###### Macro [GO\_PACKAGE\_NAME][](Name) <a name="macro_GO_PACKAGE_NAME"></a>
Override name of a Go package.

###### Macro [GO\_PROTO\_PLUGIN][](Name Ext Tool [DEPS dependencies...]) <a name="macro_GO_PROTO_PLUGIN"></a>
Define protoc plugin for GO with given Name that emits extra output with provided extension
Ext using Tool. Extra dependencies are passed via DEPS.

###### Macro [GO\_SKIP\_TESTS][](TestNames...) <a name="macro_GO_SKIP_TESTS"></a>
Define a set of tests that should not be run.
NB! Subtests are not taken into account!

###### Macro [GO\_TEST\_EMBED\_PATTERN][](PATTERN) <a name="macro_GO_TEST_EMBED_PATTERN"></a>
Define an embed pattern for internal go tests.

###### Macro [GO\_TEST\_FOR][](path/to/module)  _#builtin_ <a name="macro_GO_TEST_FOR"></a>
Produces go test for specified module

###### Macro [GO\_TEST\_SRCS][](Files...) <a name="macro_GO_TEST_SRCS"></a>
.go sources for internal tests of a module

###### Macro [GO\_XTEST\_EMBED\_PATTERN][](PATTERN) <a name="macro_GO_XTEST_EMBED_PATTERN"></a>
Define an embed pattern for external go tests.

###### Macro [GO\_XTEST\_SRCS][](Files...) <a name="macro_GO_XTEST_SRCS"></a>
.go sources for external tests of a module

###### Macro [GRADLE\_FLAGS][](flags...) _# internal_ <a name="macro_GRADLE_FLAGS"></a>
SEt additional flags for gradle

###### Macro [GRPC][]() <a name="macro_GRPC"></a>
Emit GRPC code for all .proto files in a PROTO\_LIBRARY.
This works for all available PROTO\_LIBRARY versions (C++, Python 2.x, Python 3.x, Java and Go).

###### Macro [IDEA\_EXCLUDE\_DIRS][](<excluded dirs>) <a name="macro_IDEA_EXCLUDE_DIRS"></a>
Exclude specified directories from an idea project generated by ya ide idea
Have no effect on regular build.

###### Macro [IDEA\_JAR\_SRCS][](Args...) <a name="macro_IDEA_JAR_SRCS"></a>
Not documented yet.

###### Macro [IDEA\_MODULE\_NAME][](module\_name) <a name="macro_IDEA_MODULE_NAME"></a>
Set module name in an idea project generated by ya ide idea
Have no effect on regular build.

###### Macro [IDEA\_RESOURCE\_DIRS][](<additional dirs>) <a name="macro_IDEA_RESOURCE_DIRS"></a>
Set specified resource directories in an idea project generated by ya ide idea
Have no effect on regular build.

###### Macro [IF][](condition) .. ELSEIF(other\_condition) .. ELSE() .. ENDIF()  _#builtin_ <a name="macro_IF"></a>
Apply macros if condition holds

###### Macro [INCLUDE][](filename)  _#builtin_ <a name="macro_INCLUDE"></a>
Include file textually and process it as a part of the ya.make

###### Macro [INCLUDE\_ONCE][]([yes|no])  _#builtin_ <a name="macro_INCLUDE_ONCE"></a>
Control how file is is processed if it is included into one base ya.make by multiple paths.
if `yes` passed or argument omitted, process it just once. Process each time if `no` is passed (current default)
Note: for includes from multimodules the file is processed once from each submodule (like if INCLUDEs were preprocessed into multimodule body)

###### Macro [INCLUDE\_TAGS][](tags...)  _# builtin_ <a name="macro_INCLUDE_TAGS"></a>
Additionally instantiate from multimodule all variants with tags listed (overrides default)

###### Macro [INDUCED\_DEPS][](Extension Path...)  _#builtin_ <a name="macro_INDUCED_DEPS"></a>
States that files wih the Extension generated by the PROGRAM will depend on files in Path.
This only useful in PROGRAM and similar modules. It will be applied if the PROGRAM is used in RUN\_PROGRAM macro.
All Paths specified must be absolute arcadia paths i.e. start with ${ARCADIA\_ROOT} ${ARCADIA\_BUILD\_ROOT}, ${CURDIR} or ${BINDIR}.

###### Macro [IOS\_APP\_ASSETS\_FLAGS][](Flags...) <a name="macro_IOS_APP_ASSETS_FLAGS"></a>
Not documented yet.

###### Macro [IOS\_APP\_COMMON\_FLAGS][](Flags...) <a name="macro_IOS_APP_COMMON_FLAGS"></a>
Not documented yet.

###### Macro [IOS\_APP\_SETTINGS][] <a name="macro_IOS_APP_SETTINGS"></a>
Not documented yet.

###### Macro [IOS\_ASSETS][] <a name="macro_IOS_ASSETS"></a>
Not documented yet.

###### Macro [JAR\_ANNOTATION\_PROCESSOR][](Classes...) <a name="macro_JAR_ANNOTATION_PROCESSOR"></a>
Not documented yet.

###### Macro [JAR\_EXCLUDE][](Filters...) <a name="macro_JAR_EXCLUDE"></a>
Filter .jar file content: remove matched files
\* and \*\* patterns are supported (like JAVA\_SRCS)

###### Macro [JAR\_INCLUDE][](Filters...) <a name="macro_JAR_INCLUDE"></a>
Filter .jar file content: keep only matched files
\* and \*\* patterns are supported (like JAVA\_SRCS)

###### Macro [JAR\_RESOURCE][](Id) <a name="macro_JAR_RESOURCE"></a>
Not documented yet.

###### Macro [JAVAC\_FLAGS][](Args...) <a name="macro_JAVAC_FLAGS"></a>
Set additional Java compilation flags.

###### Macro [JAVA\_DEPENDENCIES\_CONFIGURATION][](Vetos...) <a name="macro_JAVA_DEPENDENCIES_CONFIGURATION"></a>
Validate contrib/java dependencies
Valid arguments
FORBID\_DIRECT\_PEERDIRS - fail when module have direct PEERDIR (with version) (non-transitive)
FORBID\_DEFAULT\_VERSIONS - fail when module have PEERDIR to library with default (last) version (transitive)
FORBID\_CONFLICT - fail when module have resolved without DEPENDENCY\_MANAGEMENT version conflict (transitive)
FORBID\_CONFLICT\_DM - fail when module have resolved with DEPENDENCY\_MANAGEMENT version conflict (transitive)
FORBID\_CONFLICT\_DM\_RECENT - like FORBID\_CONFLICT\_DM but fail only when dependency have more recent version than specified in DEPENDENCY\_MANAGEMENT
REQUIRE\_DM - all dependencies must be specified in DEPENDENCY\_MANAGEMENT (transitive)

###### Macro [JAVA\_EXTERNAL\_DEPENDENCIES][](file1 file2 ...) <a name="macro_JAVA_EXTERNAL_DEPENDENCIES"></a>
Add non-source java external build dependency (like lombok config file)

###### Macro [JAVA\_IGNORE\_CLASSPATH\_CLASH\_FOR][]([classes]) <a name="macro_JAVA_IGNORE_CLASSPATH_CLASH_FOR"></a>
Ignore classpath clash test fails for classes

###### Macro [JAVA\_MODULE][] <a name="macro_JAVA_MODULE"></a>
Not documented yet.

###### Macro [JAVA\_PROTO\_PLUGIN][](Name Tool DEPS <Dependencies>) <a name="macro_JAVA_PROTO_PLUGIN"></a>
Define protoc plugin for Java with given Name that emits extra outputs
using Tool. Extra dependencies are passed via DEPS

###### Macro [JAVA\_RESOURCE][](JAR, SOURCES="") <a name="macro_JAVA_RESOURCE"></a>
Not documented yet.

###### Macro [JAVA\_SRCS][](srcs) <a name="macro_JAVA_SRCS"></a>
Specify java source files and resources. A macro can be contained in any of four java modules.
Keywords:
1. X SRCDIR - specify the directory x is performed relatively to search the source code for these patterns. If there is no SRCDIR, the source will be searched relative to the module directory.
2. PACKAGE\_PREFIX x - use if source paths relative to the SRCDIR does not coincide with the full class names. For example, if all sources of module are in the same package, you can create a directory package/name , and just put the source code in the SRCDIR and specify PACKAGE\_PREFIX package.name.

@example:
 - example/ya.make

       JAVA_PROGRAM()
           JAVA_SRCS(SRCDIR src/main/java **/*)
       END()

 - example/src/main/java/ru/yandex/example/HelloWorld.java

       package ru.yandex.example;
       public class HelloWorld {
            public static void main(String[] args) {
                System.out.println("Hello, World!");
            }
       }

Documentation: https://wiki.yandex-team.ru/yatool/java/#javasrcs

###### Macro [JAVA\_TEST][] <a name="macro_JAVA_TEST"></a>
Not documented yet.

###### Macro [JAVA\_TEST\_DEPS][] <a name="macro_JAVA_TEST_DEPS"></a>
Not documented yet.

###### Macro [JDK\_VERSION][](Version) <a name="macro_JDK_VERSION"></a>
Specify JDK version for module

###### Macro [JOIN\_SRCS][](Out Src...) <a name="macro_JOIN_SRCS"></a>
Join set of sources into single file named Out and send it for further processing.
This macro doesn't place all file into Out, it emits #include<Src>... Use the for C++ source files only.
You should specify file name with the extension as Out. Further processing will be done according this extension.

###### Macro [JOIN\_SRCS\_GLOBAL][](Out Src...) <a name="macro_JOIN_SRCS_GLOBAL"></a>
Join set of sources into single file named Out and send it for further processing as if it were listed as SRCS(GLOBAL Out).
This macro doesn't place all file into Out, it emits #include<Src>... Use the for C++ source files only.
You should specify file name with the extension as Out. Further processing will be done according to this extension.

###### Macro [JVM\_ARGS][](Args...) <a name="macro_JVM_ARGS"></a>
Arguments to run Java programs in tests.

Documentation: https://wiki.yandex-team.ru/yatool/test/

###### Macro [KAPT\_ANNOTATION\_PROCESSOR][](processors...) <a name="macro_KAPT_ANNOTATION_PROCESSOR"></a>
Used to specify annotation processor qualified class names.
If specified multiple times, only last specification is used.

###### Macro [KAPT\_ANNOTATION\_PROCESSOR\_CLASSPATH][](jars...) <a name="macro_KAPT_ANNOTATION_PROCESSOR_CLASSPATH"></a>
Used to specify classpath for annotation processors.
If specified multiple times, all specifications are used.

###### Macro [KAPT\_OPTS][](opts...) <a name="macro_KAPT_OPTS"></a>
Used to specify annotation processor qualified class names.
If specified multiple times, only last specification is used.

###### Macro [KOTLINC\_FLAGS][](-flags) <a name="macro_KOTLINC_FLAGS"></a>
Set additional Kotlin compilation flags.

###### Macro [LARGE\_FILES][]([AUTOUPDATED]  Files...) <a name="macro_LARGE_FILES"></a>
Use large file ether from working copy or from remote storage via placeholder <File>.external
If <File> is present locally (and not a symlink!) it will be copied to build directory.
Otherwise macro will try to locate <File>.external, parse it retrieve ot during build phase.

###### Macro [LDFLAGS][](LinkerFlags...) <a name="macro_LDFLAGS"></a>
Add flags to the link command line of executable or shared library/dll.
Note: LDFLAGS are always global. When set in the LIBRARY module they will affect all programs/dlls/tests the library is linked into.
Note: remember about the incompatibility of flags for gcc and cl.

###### Macro [LICENSE][](licenses...) <a name="macro_LICENSE"></a>
Specify the licenses of the module, separated by spaces. Specifying multiple licenses interpreted as permission to use this
library satisfying all conditions of any of the listed licenses.

A license must be prescribed for contribs

###### Macro [LICENSE\_TEXTS][](File) <a name="macro_LICENSE_TEXTS"></a>
This macro specifies the filename with all library licenses texts

###### Macro [LINKER\_SCRIPT][](Files...) <a name="macro_LINKER_SCRIPT"></a>
Specify files to be used as a linker script

###### Macro [LINK\_EXEC\_DYN\_LIB\_IMPL][] <a name="macro_LINK_EXEC_DYN_LIB_IMPL"></a>
$usage: LINK\_EXEC\_DYN\_LIB\_IMPL(peers...) # internal

###### Macro [LINK\_EXE\_IMPL][] <a name="macro_LINK_EXE_IMPL"></a>
$usage: LINK\_EXE\_IMPL(peers...) # internal

###### Macro [LINT][](<none|base|strict>) <a name="macro_LINT"></a>
Set linting level for sources of the module

###### Macro [LJ\_21\_ARCHIVE][](NAME Name LuaFiles...) _# deprecated_ <a name="macro_LJ_21_ARCHIVE"></a>
Precompile .lua files using LuaJIT 2.1 and archive both sources and results using sources names as keys

###### Macro [LJ\_ARCHIVE][](NAME Name LuaFiles...) <a name="macro_LJ_ARCHIVE"></a>
Precompile .lua files using LuaJIT and archive both sources and results using sources names as keys

###### Macro [LLVM\_BC][] <a name="macro_LLVM_BC"></a>
Not documented yet.

###### Macro [LLVM\_COMPILE\_C][](Input Output Opts...) <a name="macro_LLVM_COMPILE_C"></a>
Emit LLVM bytecode from .c file. BC\_CFLAGS, LLVM\_OPTS and C\_FLAGS\_PLATFORM are passed in, while CFLAGS are not.
Note: Output name is used as is, no extension added.

###### Macro [LLVM\_COMPILE\_CXX][](Input Output Opts...) <a name="macro_LLVM_COMPILE_CXX"></a>
Emit LLVM bytecode from .cpp file. BC\_CXXFLAGS, LLVM\_OPTS and C\_FLAGS\_PLATFORM are passed in, while CFLAGS are not.
Note: Output name is used as is, no extension added.

###### Macro [LLVM\_COMPILE\_LL][](Input Output Opts...) <a name="macro_LLVM_COMPILE_LL"></a>
Compile LLVM bytecode to object representation.
Note: Output name is used as is, no extension added.

###### Macro [LLVM\_LINK][](Output Inputs...) <a name="macro_LLVM_LINK"></a>
Call llvm-link on set of Inputs to produce Output.
Note: Unlike many other macros output argument goes first. Output name is used as is, no extension added.

###### Macro [LLVM\_OPT][](Input Output Opts...) <a name="macro_LLVM_OPT"></a>
Call llvm-opt with set of Opts on Input to produce Output.
Note: Output name is used as is, no extension added.

###### Macro [LOCAL\_JAR][](File) <a name="macro_LOCAL_JAR"></a>
Not documented yet.

###### Macro [LOCAL\_SOURCES\_JAR][](File) <a name="macro_LOCAL_SOURCES_JAR"></a>
Not documented yet.

###### Macro [MACROS\_WITH\_ERROR][] <a name="macro_MACROS_WITH_ERROR"></a>
Not documented yet.

###### Macro [MANUAL\_GENERATION][](Outs...) <a name="macro_MANUAL_GENERATION"></a>
Not documented yet.

###### Macro [MAPKITIDL][](idl-file-name... <a name="macro_MAPKITIDL"></a>
[OUT\_DIR output-dir]
[IDL\_INCLUDES idl-dirs...]
[FILTER filters...])
[FILTER\_OUT filters...])
[GLOBAL\_OUTPUTS]
Generate bindings to target platform language.
(Used for mobile MapKit project)
1. idl-file-name... - a list of \*.idl files to process
2. output-dir - a base root of output directory
3. idl-dirs - a list of directories where to search for imported \*.idl files
4. filters - a list of extensions used to filter outputs and output includes

###### Macro [MAPKIT\_ADDINCL][](Dirs...) <a name="macro_MAPKIT_ADDINCL"></a>
Not documented yet.

###### Macro [MAPKIT\_ENABLE\_WHOLE\_ARCHIVE][]() _# internal deprecated_ <a name="macro_MAPKIT_ENABLE_WHOLE_ARCHIVE"></a>
This macro is strictly prohibited to use outside of mapsmobi project

###### Macro [MAPSMOBI\_COLLECT\_AIDL\_FILES][](varname [dir]) _# internal_ <a name="macro_MAPSMOBI_COLLECT_AIDL_FILES"></a>
This macro is strictly prohibited to use outside of mapsmobi project

###### Macro [MAPSMOBI\_COLLECT\_ASSETS\_FILES][](varname [dir]) _# internal_ <a name="macro_MAPSMOBI_COLLECT_ASSETS_FILES"></a>
This macro is strictly prohibited to use outside of mapsmobi project

###### Macro [MAPSMOBI\_COLLECT\_JAVA\_FILES][](varname [dir]) _# internal_ <a name="macro_MAPSMOBI_COLLECT_JAVA_FILES"></a>
This macro is strictly prohibited to use outside of mapsmobi project

###### Macro [MAPSMOBI\_COLLECT\_JNI\_LIBS\_FILES][](varname [dir]) _# internal_ <a name="macro_MAPSMOBI_COLLECT_JNI_LIBS_FILES"></a>
This macro is strictly prohibited to use outside of mapsmobi project

###### Macro [MAPSMOBI\_COLLECT\_RES\_FILES][](varname [dir]) _# internal_ <a name="macro_MAPSMOBI_COLLECT_RES_FILES"></a>
This macro is strictly prohibited to use outside of mapsmobi project

###### Macro [MAPSMOBI\_COLLECT\_TPL\_FILES][](varname [dir]) _# internal_ <a name="macro_MAPSMOBI_COLLECT_TPL_FILES"></a>
This macro is strictly prohibited to use outside of mapsmobi project

###### Macro [MAPSMOBI\_SRCS][](filenames...) _# internal_ <a name="macro_MAPSMOBI_SRCS"></a>
Make all source files listed as GLOBAL or not (depending on the value of
MAPSMOBI\_USE\_SRCS\_GLOBAL). Be careful since the value of
MAPSMOBI\_USE\_SRCS\_GLOBAL matters! If the value of this variable is equal to
GLOBAL then call to MAPSMOBI\_SRCS() macro behaves like call to
GLOBAL\_SRCS() macro otherwise the value of MAPSMOBI\_USE\_SRCS\_GLOBAL is
treated as a file name and a call to MAPSMOBI\_SRCS() macro behaves like a
call to SRCS() macro with additional argument which is the value of
MAPSMOBI\_USE\_SRCS\_GLOBAL variable

###### Macro [MAPS\_GARDEN\_COLLECT\_MODULE\_TRAITS][](varnamei dir) _# internal_ <a name="macro_MAPS_GARDEN_COLLECT_MODULE_TRAITS"></a>
This macro is strictly prohibited to use outside of maps/garden project

###### Macro [MAPS\_IDL\_ADDINCL][](dirnames...) _# internal_ <a name="macro_MAPS_IDL_ADDINCL"></a>
Warpper for MAPKIT\_ADDINCL macro which is used for mobile mapkit build

###### Macro [MAPS\_IDL\_GLOBAL\_SRCS][](filenames...) _# internal_ <a name="macro_MAPS_IDL_GLOBAL_SRCS"></a>
Warpper for MAPKITIDL macro which is used for mobile mapkit build

###### Macro [MAPS\_IDL\_SRCS][](filenames...) _# internal_ <a name="macro_MAPS_IDL_SRCS"></a>
Warpper for MAPKITIDL macro which is used for mobile mapkit build

###### Macro [MASMFLAGS][](compiler flags) <a name="macro_MASMFLAGS"></a>
Add the specified flags to the compilation command of .masm files.

###### Macro [MAVEN\_GROUP\_ID][](group\_id\_for\_maven\_export) <a name="macro_MAVEN_GROUP_ID"></a>
Set maven export group id for JAVA\_PROGRAM() and JAVA\_LIBRARY().
Have no effect on regular build.

###### Macro [MESSAGE][]([severity] message)  _# builtin_ <a name="macro_MESSAGE"></a>
Print message with given severity level (STATUS, FATAL\_ERROR)

###### Macro [MOBILE\_TEST\_APK\_AAR\_AARS][](filenames...) _# internal_ <a name="macro_MOBILE_TEST_APK_AAR_AARS"></a>
Not documented yet.

###### Macro [MOBILE\_TEST\_APK\_AAR\_BUNDLES][](filenames...) _# internal_ <a name="macro_MOBILE_TEST_APK_AAR_BUNDLES"></a>
Not documented yet.

###### Macro [MOBILE\_TEST\_APK\_AAR\_MANIFEST][](file) _# internal_ <a name="macro_MOBILE_TEST_APK_AAR_MANIFEST"></a>
Not documented yet.

###### Macro [MOBILE\_TEST\_APK\_AAR\_PROGUARD\_RULES][](file) _# internal_ <a name="macro_MOBILE_TEST_APK_AAR_PROGUARD_RULES"></a>
Not documented yet.

###### Macro [MOBILE\_TEST\_APK\_TEMPLATE][](dir filenames...) _# internal_ <a name="macro_MOBILE_TEST_APK_TEMPLATE"></a>
Not documented yet.

###### Macro [MSVC\_FLAGS][]([GLOBAL compiler\_flag]\* compiler\_flags) <a name="macro_MSVC_FLAGS"></a>
Add the specified flags to the compilation line of C/C++files.
Flags apply only if the compiler used is MSVC (cl.exe)

###### Macro [MX\_FORMULAS][](BinFiles...) _# deprecated, matrixnet_ <a name="macro_MX_FORMULAS"></a>
Create MatrixNet formulas archive

###### Macro [NEED\_CHECK][]() <a name="macro_NEED_CHECK"></a>
Commits to the project marked with this macro will be blocked by pre-commit check and then will be
automatically merged to trunk only if there is no new broken build targets in check results.
The use of this macro is disabled by default.

###### Macro [NEED\_REVIEW][]() _# deprecated_ <a name="macro_NEED_REVIEW"></a>
Mark the project as needing review.
Reviewers are listed in the macro OWNER. The use of this macro is disabled by default.
Details can be found here: https://clubs.at.yandex-team.ru/arcadia/6104

###### Macro [NGINX\_MODULES][](Modules...) <a name="macro_NGINX_MODULES"></a>
Not documented yet.

###### Macro [NODE\_MODULES][]() <a name="macro_NODE_MODULES"></a>
Materializes `node\_modules.tar` bundle according to the module's lockfile.

@see [NPM\_CONTRIBS()](#module\_NPM\_CONTRIBS)

###### Macro [NO\_BUILD\_IF][](variables)  _# builtin_ <a name="macro_NO_BUILD_IF"></a>
Print warning if some variable is true

###### Macro [NO\_CHECK\_IMPORTS][]([patterns]) <a name="macro_NO_CHECK_IMPORTS"></a>
Do not run checks on imports of Python modules.
Optional parameter mask patterns describes the names of the modules that do not need to check.

###### Macro [NO\_CLANG\_COVERAGE][]() <a name="macro_NO_CLANG_COVERAGE"></a>
Disable heavyweight clang coverage for the module

###### Macro [NO\_CLANG\_TIDY][]() <a name="macro_NO_CLANG_TIDY"></a>
Not documented yet.

###### Macro [NO\_CODENAVIGATION][]() _# internal_ <a name="macro_NO_CODENAVIGATION"></a>
Disable codenaviagtion for a module. Needed to avoid PEERDIR loops in codenavigation support.
Most probably you'll never need this. If you think you need, please contact devtools@ for assistance.

###### Macro [NO\_COMPILER\_WARNINGS][]() <a name="macro_NO_COMPILER_WARNINGS"></a>
Disable all compiler warnings in the module.
Priorities: NO\_COMPILER\_WARNINGS > NO\_WERROR > WERROR\_MODE > WERROR.

###### Macro [NO\_CPU\_CHECK][]() <a name="macro_NO_CPU_CHECK"></a>
Compile module without startup CPU features check

###### Macro [NO\_CYTHON\_COVERAGE][]() <a name="macro_NO_CYTHON_COVERAGE"></a>
Disable cython and cythonized python coverage (CYTHONIZE\_PY)
Implies NO\_CLANG\_COVERAGE() - right now, we can't disable instrumentation for .py.cpp files, but enable for .cpp

###### Macro [NO\_DEBUG\_INFO][]() <a name="macro_NO_DEBUG_INFO"></a>
Compile files without debug info collection.

###### Macro [NO\_DOCTESTS][]() <a name="macro_NO_DOCTESTS"></a>
Disable doctests in PY[|3|23\_]TEST

###### Macro [NO\_EXPORT\_DYNAMIC\_SYMBOLS][]() <a name="macro_NO_EXPORT_DYNAMIC_SYMBOLS"></a>
Disable exporting all non-hidden symbols as dynamic when linking a PROGRAM.

###### Macro [NO\_EXTENDED\_SOURCE\_SEARCH][]() <a name="macro_NO_EXTENDED_SOURCE_SEARCH"></a>
Prevent module using in extended python source search.
Use the macro if module contains python2-only files (or other python sources which shouldn't be imported by python3 interpreter)
which resides in the same directories with python 3 useful code. contrib/python/future is a example.
Anyway, preferred way is to move such files into separate dir and don't use this macro at all.

Also see: https://docs.yandex-team.ru/ya-make/manual/python/vars#y\_python\_extended\_source\_search for details

###### Macro [NO\_JOIN\_SRC][]() _# deprecated, does-nothing_ <a name="macro_NO_JOIN_SRC"></a>
This macro currently does nothing. This is default behavior which cannot be overridden at module level.

###### Macro [NO\_LIBC][]() <a name="macro_NO_LIBC"></a>
Exclude dependencies on C++ and C runtimes (including util, musl and libeatmydata).
Note: use this with care. libc most likely will be linked into executable anyway,
so using libc headers/functions may not be detected at build time and may lead to unpredictable behavors at configure time.

###### Macro [NO\_LINT][]([ktlint]) <a name="macro_NO_LINT"></a>
Do not check for style files included in PY\_SRCS, TEST\_SRCS, JAVA\_SRCS.
Ktlint can be disabled using NO\_LINT(ktlint) explicitly.

###### Macro [NO\_LTO][]() <a name="macro_NO_LTO"></a>
Disable any lto (link-time optimizations) for the module.
This will compile module source files as usual (without LTO) but will not prevent lto-enabled
linking of entire program if global settings say so.

###### Macro [NO\_MYPY][]() <a name="macro_NO_MYPY"></a>
Not documented yet.

###### Macro [NO\_NEED\_CHECK][]() <a name="macro_NO_NEED_CHECK"></a>
Commits to the project marked with this macro will not be affected by higher-level NEED\_CHECK macro.

###### Macro [NO\_OPTIMIZE][]() <a name="macro_NO_OPTIMIZE"></a>
Build code without any optimizations (-O0 mode).

###### Macro [NO\_OPTIMIZE\_PY\_PROTOS][]() <a name="macro_NO_OPTIMIZE_PY_PROTOS"></a>
Disable Python proto optimization using embedding corresponding C++ code into binary.
Python protobuf runtime will use C++ implementation instead of Python one if former is available.
This is default mode only for some system libraries.

###### Macro [NO\_PLATFORM][]() <a name="macro_NO_PLATFORM"></a>
Exclude dependencies on C++ and C runtimes (including util, musl and libeatmydata) and set NO\_PLATFORM variable for special processing.
Note: use this with care. libc most likely will be linked into executable anyway,
so using libc headers/functions may not be detected at build time and may lead to unpredictable behavors at configure time.

###### Macro [NO\_PLATFORM\_RESOURCES][]() _# internal_ <a name="macro_NO_PLATFORM_RESOURCES"></a>
Exclude dependency on platform resources libraries.
Most probably you'll never need this. If you think you need, please contact devtools@ for assistance.

###### Macro [NO\_PYTHON\_COVERAGE][]() <a name="macro_NO_PYTHON_COVERAGE"></a>
Disable python coverage for module

###### Macro [NO\_PYTHON\_INCLUDES][]() _# internal_ <a name="macro_NO_PYTHON_INCLUDES"></a>
Disable dependencies on libraries providing Python headers.
This is only used in Python libraries themselves to avoid PEERDIR loops.

###### Macro [NO\_RUNTIME][]() <a name="macro_NO_RUNTIME"></a>
This macro:
1. Sets the ENABLE(NOUTIL) + DISABLE(USE\_INTERNAL\_STL);
2. If the project that contains the macro NO\_RUNTIME(), peerdir-it project does not contain NO\_RUNTIME() => Warning.
Note: use this with care. Arcadia STL most likely will be linked into executable anyway, so using STL headers/functions/classes
may not be detected at build time and may lead to unpredictable behavors at configure time.

###### Macro [NO\_SANITIZE][]() <a name="macro_NO_SANITIZE"></a>
Disable all sanitizers for the module.

###### Macro [NO\_SANITIZE\_COVERAGE][]() <a name="macro_NO_SANITIZE_COVERAGE"></a>
Disable lightweight coverage (-fsanitize-coverage) for the module.

###### Macro [NO\_SSE4][]() <a name="macro_NO_SSE4"></a>
Compile module without SSE4

###### Macro [NO\_UTIL][]() <a name="macro_NO_UTIL"></a>
Build module without dependency on util.
Note: use this with care. Util most likely will be linked into executable anyway,
so using util headers/functions/classes may not be detected at build time and may lead to unpredictable behavors at configure time.

###### Macro [NO\_WERROR][]() <a name="macro_NO_WERROR"></a>
Override WERROR() behavior
Priorities: NO\_COMPILER\_WARNINGS > NO\_WERROR > WERROR\_MODE > WERROR.

###### Macro [NO\_WSHADOW][]() <a name="macro_NO_WSHADOW"></a>
Disable C++ shadowing warnings.

###### Macro [NVCC\_DEVICE\_LINK][](file.cu...) <a name="macro_NVCC_DEVICE_LINK"></a>
Run nvcc --device-link on objects compiled from srcs with --device-c.
This generates a stub object devlink.o that supplies missing pieces for the
host linker to link relocatable device objects into the final executable.

###### Macro [ONLY\_TAGS][](tags...)  _# builtin_ <a name="macro_ONLY_TAGS"></a>
Instantiate from multimodule only variants with tags listed

###### Macro [OPENSOURCE\_EXPORT\_REPLACEMENT][](CMAKE PkgName CMAKE\_TARGET PkgName::PkgTarget CONAN ConanRef CMAKE\_COMPONENT OptCmakePkgComponent) <a name="macro_OPENSOURCE_EXPORT_REPLACEMENT"></a>
Use specified conan/system pacakcge when exporting cmake build scripts for arcadia C++ project
for opensource publication.

###### Macro [OPTIMIZE\_PY\_PROTOS][]()  _# internal_ <a name="macro_OPTIMIZE_PY_PROTOS"></a>
Enable Python proto optimization by embedding corresponding C++ code into binary.
Python protobuf runtime will use C++ implementation instead of Python one if former is available.
This is default mode for most PROTO\_LIBRARY's and PY2\_LIBRARY's, some system ones being exceptions.

###### Macro [ORIGINAL\_SOURCE][](Source) <a name="macro_ORIGINAL_SOURCE"></a>
This macro specifies the source repository for contrib
Does nothing now (just a placeholder for future functionality)
See https://st.yandex-team.ru/DTCC-316

###### Macro [OWNER][](owners...)  _# builtin_ <a name="macro_OWNER"></a>
Add reviewers/responsibles of the code.
In the OWNER macro you can use:
1. login-s from staff.yandex-team.ru
2. Review group (to specify the Code-review group need to use the prefix g:)

Ask devtools@yandex-team.ru if you need more information

###### Macro [PACK][](archive\_type) <a name="macro_PACK"></a>
When placed inside the PACKAGE module, packs the build results tree to the archive with specified extension. Currently supported extensions are `tar` and `tar.gz`

Is not allowed other module types than PACKAGE().

@see: [PACKAGE()](#module\_PACKAGE)

###### Macro [PACKAGE\_STRICT][]() <a name="macro_PACKAGE_STRICT"></a>
Not documented yet.

###### Macro [PACK\_GLOBALS\_IN\_LIBRARY][]() <a name="macro_PACK_GLOBALS_IN_LIBRARY"></a>
Not documented yet.

###### Macro [PARTITIONED\_RECURSE][]([BALANCING\_CONFIG config] dirs...)  _# builtin_ <a name="macro_PARTITIONED_RECURSE"></a>
Add directories to the build
All projects must be reachable from the root chain RECURSE() for monorepo continuous integration functionality.
Arguments are processed in chunks

###### Macro [PARTITIONED\_RECURSE\_FOR\_TESTS][]([BALANCING\_CONFIG config] dirs...)  _# builtin_ <a name="macro_PARTITIONED_RECURSE_FOR_TESTS"></a>
Add directories to the build if tests are demanded.
Arguments are processed in chunks

###### Macro [PARTITIONED\_RECURSE\_ROOT\_RELATIVE][]([BALANCING\_CONFIG config] dirlist)  _# builtin_ <a name="macro_PARTITIONED_RECURSE_ROOT_RELATIVE"></a>
In comparison with RECURSE(), in dirlist there must be a directory relative to the root (${ARCADIA\_ROOT}).
Arguments are processed in chunks

###### Macro [PEERDIR][](dirs...)  _# builtin_ <a name="macro_PEERDIR"></a>
Specify project dependencies
Indicates that the project depends on all of the projects from the list of dirs.
Libraries from these directories will be collected and linked to the current target if the target is executable or sharedlib/dll.
If the current target is a static library, the specified directories will not be built, but they will be linked to any executable target that will link the current library.
@params:
1. As arguments PEERDIR you can only use the LIBRARY directory (the directory with the PROGRAM/DLL and derived from them are prohibited to use as arguments PEERDIR).
2. ADDINCL Keyword ADDINCL (written before the specified directory), adds the flag -I<path to library> the flags to compile the source code of the current project.
Perhaps it may be removed in the future (in favor of a dedicated ADDINCL)

###### Macro [PIRE\_INLINE][](FILES...) <a name="macro_PIRE_INLINE"></a>
Not documented yet.

###### Macro [PIRE\_INLINE\_CMD][](SRC) <a name="macro_PIRE_INLINE_CMD"></a>
Not documented yet.

###### Macro [PREPARE\_INDUCED\_DEPS][](VAR Type Files...) <a name="macro_PREPARE_INDUCED_DEPS"></a>
Format value for `INDUCED\_DEPS` param in certain macros and assign to `VAR`
This tells that files of Type resulted from code generation macros (not neccessarily directly,
but in processing chain of generated files) should have extra dependencies from list of Files...

Prominent example here is Cython: one can generate .pyx file that may depend on .pxd and have cimpot from
certain .h. The former is dependency for .pyx itself, while the latter is dependency for .pyx.cpp
resulted from Cython-processing of generated pyx. The code ganeration will look like:
```
PREPARE_INDUCED_DEPS(PYX_DEPS pyx imported.pxd)
PREPARE_INDUCED_DEPS(CPP_DEPS cpp cdefed.h)
RUN_PYTHON3(generate_pyx.py genereted.pyx OUT generated.pyx INDUCED_DEPS $PYX_DEPS $CPP_DEPS)
```

The VAR will basically contain pair of `Type:[Files...]` in a form suitable for passing
as an element of array parameter. This is needed because language of ya.make doesn't support
Dict params right now and so it is impossible to directly pass something
like `{Type1:[Files2...], Type2:[Files2...]}`

###### Macro [PRIMARY\_OUTPUT][]\_VALUE(Output) _# internal_ <a name="macro_PRIMARY_OUTPUT"></a>
The use of this module is strictly prohibited!!!

###### Macro [PRINT\_MODULE\_TYPE][] <a name="macro_PRINT_MODULE_TYPE"></a>
Not documented yet.

###### Macro [PROCESS\_DOCS][] <a name="macro_PROCESS_DOCS"></a>
Not documented yet.

###### Macro [PROCESS\_MKDOCS][] <a name="macro_PROCESS_MKDOCS"></a>
Not documented yet.

###### Macro [PROGUARD\_RULES][](ProguardRuleFiles...) <a name="macro_PROGUARD_RULES"></a>
This macro is strictly prohibited to use outside of mapsmobi project

###### Macro [PROTO2FBS][](InputProto) <a name="macro_PROTO2FBS"></a>
Produce flatbuf schema out of protobuf description.

###### Macro [PROTO\_ADDINCL][]([GLOBAL] [WITH\_GEN] Path) <a name="macro_PROTO_ADDINCL"></a>
This macro introduces proper ADDINCLs for .proto-files found in sources and
.cpp/.h generated files, supplying them to appropriate commands and allowing
proper dependency resolution at configure-time.

Note: you normally shouldn't use this macro. ADDINCLs should be sent to user
from dependency via PROTO\_NAMESPACE macro

###### Macro [PROTO\_NAMESPACE][]([GLOBAL] [WITH\_GEN] Namespace) <a name="macro_PROTO_NAMESPACE"></a>
Defines protobuf namespace (import/export path prefix) which should be used for imports and
which defines output path for .proto generation.

For proper importing and configure-time dependency management it sets ADDINCLs
for both .cpp headers includes and .proto imports. If .proto expected to be used outside of the
processing module use GLOBAL to send proper ADDINCLs to all (transitive) users. PEERDIR to
PROTO\_LIBRARY with PROTO\_NAMESPACE(GLOBAL ) is enough at user side to correctly use the library.
If generated .proto files are going to be used for building a module than use of WITH\_GEN
parameter will add appropriate dir from the build root for .proto files search.

###### Macro [PROVIDES][](Name...) <a name="macro_PROVIDES"></a>
Specifies provided features. The names must be correct C identifiers.
This prevents different libraries providing the same features to be linked into one program.

###### Macro [PYTHON][](script\_path args... [CWD dir] [ENV key=value...] [TOOL tools...] [IN[\_NOPARSE] inputs...] [OUT[\_NOAUTO] outputs...] [STDOUT[\_NOAUTO] output] [OUTPUT\_INCLUDES output\_includes...] [INDUCED\_DEPS $VARs...]) <a name="macro_PYTHON"></a>
Run a python script with $(PYTHON)/python built from devtools/huge\_python.
These macros are similar: RUN\_PROGRAM, RUN\_LUA, PYTHON.

Parameters:
- script\_path - Path to the script.
- args... - Program arguments. Relative paths listed in TOOL, IN, OUT, STDOUT become absolute.
- CWD dir - Absolute path of the working directory.
- ENV key=value... - Environment variables.
- TOOL tools... - Auxiliary tool directories.
- IN[\_NOPARSE] inputs... - Input files. NOPARSE inputs are treated as textual and not parsed for dependencies regardless of file extensions.
- OUT[\_NOAUTO] outputs... - Output files. NOAUTO outputs are not automatically added to the build process.
- STDOUT[\_NOAUTO] output - Redirect the standard output to the output file.
- OUTPUT\_INCLUDES output\_includes... - Includes of the output files that are needed to build them.
- INDUCED\_DEPS $VARs... - Dependencies for generated files. Unlike `OUTPUT\_INCLUDES` these may target files further in processing chain.
                          In order to do so VAR should be filled by PREPARE\_INDUCED\_DEPS macro, stating target files (by type) and set of dependencies

For absolute paths use ${ARCADIA\_ROOT} and ${ARCADIA\_BUILD\_ROOT}, or
${CURDIR} and ${BINDIR} which are expanded where the outputs are used.

###### Macro [PYTHON2\_ADDINCL][]() <a name="macro_PYTHON2_ADDINCL"></a>
This macro adds include path for Python headers (Python 2.x variant) without PEERDIR.
This should be used in 2 cases only:
- In PY2MODULE since it compiles into .so and uses external Python runtime;
- In system Python libraries themselves since proper PEERDIR there may create a loop;
In all other cases use USE\_PYTHON2 macro instead.

Never use this macro in PY2\_PROGRAM, PY2\_LIBRARY and PY23\_LIBRARY: they have everything needed by default.

Documentation: https://wiki.yandex-team.ru/devtools/commandsandvars/py\_srcs

###### Macro [PYTHON2\_MODULE][]() <a name="macro_PYTHON2_MODULE"></a>
Use in PY\_ANY\_MODULE to set it up for Python 2.x.

###### Macro [PYTHON3\_ADDINCL][]() <a name="macro_PYTHON3_ADDINCL"></a>
This macro adds include path for Python headers (Python 3.x variant).
This should be used in 2 cases only:
- In PY2MODULE since it compiles into .so and uses external Python runtime;
- In system Python libraries themselves since peerdir there may create a loop;
In all other cases use USE\_PYTHON3() macro instead.

Never use this macro in PY3\_PROGRAM and PY3\_LIBRARY and PY23\_LIBRARY: they have everything by default.

Documentation: https://wiki.yandex-team.ru/devtools/commandsandvars/py\_srcs

###### Macro [PYTHON3\_MODULE][]() <a name="macro_PYTHON3_MODULE"></a>
Use in PY\_ANY\_MODULE to set it up for Python 3.x.

###### Macro [PYTHON\_PATH][](Path) <a name="macro_PYTHON_PATH"></a>
Set path to Python that will be used to runs scripts in tests

###### Macro [PY\_CONSTRUCTOR][](package.module[:func]) <a name="macro_PY_CONSTRUCTOR"></a>
Specifies the module or function which will be started before python's main()
init() is expected in the target module if no function is specified
Can be considered as \_\_attribute\_\_((constructor)) for python

###### Macro [PY\_DOCTESTS][](Packages...) <a name="macro_PY_DOCTESTS"></a>
Add to the test doctests for specified Python packages
The packages should be part of a test (listed as sources of the test or its PEERDIRs).

###### Macro [PY\_ENUMS\_SERIALIZATION][] <a name="macro_PY_ENUMS_SERIALIZATION"></a>
Not documented yet.

###### Macro [PY\_EXTRA\_LINT\_FILES][](files...) <a name="macro_PY_EXTRA_LINT_FILES"></a>
Add extra Python files for linting. This macro allows adding
Python files which has no .py extension.

###### Macro [PY\_MAIN][](package.module[:func]) <a name="macro_PY_MAIN"></a>
Specifies the module or function from which to start executing a python program

Documentation: https://wiki.yandex-team.ru/arcadia/python/pysrcs/#modulipyprogrampy3programimakrospymain

###### Macro [PY\_NAMESPACE][](prefix) <a name="macro_PY_NAMESPACE"></a>
Sets default Python namespace for all python sources in the module.
Especially suitable in PROTO\_LIBRARY where Python sources are generated and there is no PY\_SRCS to place NAMESPACE parameter.

###### Macro [PY\_PROTOS\_FOR][](path/to/module)  _#builtin, deprecated_ <a name="macro_PY_PROTOS_FOR"></a>
Use PROTO\_LIBRARY() in order to have .proto compiled into Python.
Generates pb2.py files out of .proto files and saves those into PACKAGE module

###### Macro [PY\_PROTO\_PLUGIN][](Name Ext Tool DEPS <Dependencies>) <a name="macro_PY_PROTO_PLUGIN"></a>
Define protoc plugin for python with given Name that emits extra output with provided Extension
using Tool. Extra dependencies are passed via DEPS

###### Macro [PY\_PROTO\_PLUGIN2][](Name Ext1 Ext2 Tool DEPS <Dependencies>) <a name="macro_PY_PROTO_PLUGIN2"></a>
Define protoc plugin for python with given Name that emits 2 extra outputs with provided Extensions
using Tool. Extra dependencies are passed via DEPS

###### Macro [PY\_REGISTER][]([package.]module\_name) <a name="macro_PY_REGISTER"></a>
Python knows about which built-ins can be imported, due to their registration in the Assembly or at the start of the interpreter.
All modules from the sources listed in PY\_SRCS() are registered automatically.
To register the modules from the sources in the SRCS(), you need to use PY\_REGISTER().

PY\_REGISTER(module\_name) initializes module globally via call to initmodule\_name()
PY\_REGISTER(package.module\_name) initializes module in the specified package
It renames its init function with CFLAGS(-Dinitmodule\_name=init7package11module\_name)
or CFLAGS(-DPyInit\_module\_name=PyInit\_7package11module\_name)

Documentation: https://wiki.yandex-team.ru/arcadia/python/pysrcs/#makrospyregister

###### Macro [PY\_SRCS][]({| CYTHON\_C} { | TOP\_LEVEL | NAMESPACE ns} Files...) <a name="macro_PY_SRCS"></a>
Build specified Python sources according to Arcadia binary Python build. Basically creates precompiled and source resources keyed with module paths.
The resources eventually are linked into final program and can be accessed as regular Python modules.
This custom loader linked into the program will add them to sys.meta\_path.

PY\_SRCS also support .proto, .ev, .pyx and .swg files. The .proto and .ev are compiled to .py-code by protoc and than handled as usual .py files.
.pyx and .swg lead to C/C++ Python extensions generation, that are automatically registered in Python as built-in modules.

By default .pyx files are built as C++-extensions. Use CYTHON\_C to build them as C (similar to BUILDWITH\_CYTHON\_C, but with the ability to specify namespace).

\_\_init\_\_.py never required, but if present (and specified in PY\_SRCS), it will be imported when you import package modules with \_\_init\_\_.py Oh.

@example

    PY2_LIBRARY(mymodule)
        PY_SRCS(a.py sub/dir/b.py e.proto sub/dir/f.proto c.pyx sub/dir/d.pyx g.swg sub/dir/h.swg)
    END()

PY\_SRCS honors Python2 and Python3 differences and adjusts itself to Python version of a current module.
PY\_SRCS can be used in any Arcadia Python build modules like PY\*\_LIBRARY, PY\*\_PROGRAM, PY\*TEST.
PY\_SRCS in LIBRARY or PROGRAM effectively converts these into PY2\_LIBRARY and PY2\_PROGRAM respectively.
It is strongly advised to make this conversion explicit. Never use PY\_SRCS in a LIBRARY if you plan to use it from external Python extension module.

Documentation: https://wiki.yandex-team.ru/arcadia/python/pysrcs/#modulipylibrarypy3libraryimakrospysrcs

###### Macro [PY\_SSQLS\_SRCS][](Srcs...) <a name="macro_PY_SSQLS_SRCS"></a>
Not documented yet.

###### Macro [REAL\_LINK\_DYN\_LIB\_IMPL][] <a name="macro_REAL_LINK_DYN_LIB_IMPL"></a>
$usage: REAL\_LINK\_DYN\_LIB\_IMPL(peers...) # internal

###### Macro [REAL\_LINK\_EXEC\_DYN\_LIB\_IMPL][] <a name="macro_REAL_LINK_EXEC_DYN_LIB_IMPL"></a>
$usage: REAL\_LINK\_EXEC\_DYN\_LIB\_IMPL(peers...) # internal

###### Macro [REAL\_LINK\_EXE\_IMPL][] <a name="macro_REAL_LINK_EXE_IMPL"></a>
$usage: REAL\_LINK\_EXE\_IMPL(peers...) # internal

###### Macro [RECURSE][](dirs...)  _# builtin_ <a name="macro_RECURSE"></a>
Add directories to the build
All projects must be reachable from the root chain RECURSE() for monorepo continuous integration functionality

###### Macro [RECURSE\_FOR\_TESTS][](dirs...)  _# builtin_ <a name="macro_RECURSE_FOR_TESTS"></a>
Add directories to the build if tests are demanded.
Use --force-build-depends flag if you want to build testing modules without tests running

###### Macro [RECURSE\_ROOT\_RELATIVE][](dirlist)  _# builtin_ <a name="macro_RECURSE_ROOT_RELATIVE"></a>
In comparison with RECURSE(), in dirlist there must be a directory relative to the root (${ARCADIA\_ROOT})

###### Macro [REGISTER\_SANDBOX\_IMPORT][] <a name="macro_REGISTER_SANDBOX_IMPORT"></a>
Not documented yet.

###### Macro [REGISTER\_YQL\_PYTHON\_UDF][] <a name="macro_REGISTER_YQL_PYTHON_UDF"></a>
Not documented yet.

###### Macro [REQUIREMENTS][]([cpu:<count>] [disk\_usage:<size>] [ram:<size>] [ram\_disk:<size>] [container:<id>] [network:<restricted|full>] [dns:dns64]) <a name="macro_REQUIREMENTS"></a>
Allows you to specify the requirements of the test.

Documentation about the Arcadia test system: https://wiki.yandex-team.ru/yatool/test/

###### Macro [REQUIRES][](dirs...) <a name="macro_REQUIRES"></a>
Specify list of dirs which this module must depend on indirectly.

This macro can be used if module depends on the directories specified but they can't be listed
as direct PEERDIR dependencies (due to public include order or link order issues).

###### Macro [RESOLVE\_PROTO][]() <a name="macro_RESOLVE_PROTO"></a>
Enable include resolving within UNIONs and let system .proto being resolved
among .proto/.gztproto imports

Note: it is currently impossible to enable resolving only for .proto, so resolving is enabled for all supported files
also we only add ADDINCL for stock protobuf. So use this macro with care: it may cause resolving problems those are
to be addressed by either ADDINCLs or marking them as TEXT. Please contact devtools for details.

###### Macro [RESOURCE][]([FORCE\_TEXT ][Src Key]\* [- Key=Value]\*) _# built-in_ <a name="macro_RESOURCE"></a>
Add data (resources, random files, strings) to the program)
The common usage is to place Src file into binary. The Key is used to access it using library/cpp/resource or library/python/resource.
Alternative syntax with '- Key=Value' allows placing Value string as resource data into binary and make it accessible by Key.

This is a simpler but less flexible option than ARCHIVE(), because in the case of ARCHIVE(), you have to use the data explicitly,
and in the case of RESOURCE(), the data will fall through SRCS() or SRCS(GLOBAL) to binary linking.

Use the FORCE\_TEXT parameter to explicitly mark all Src files as text files: they will not be parsed unless used elsewhere.

@example: https://wiki.yandex-team.ru/yatool/howtowriteyamakefiles/#a2ispolzujjtekomanduresource

@example:

    LIBRARY()
        OWNER(user1)

        RESOURCE(
            path/to/file1 /key/in/program/1
            path/to/file2 /key2
        )
    END()

###### Macro [RESOURCE\_FILES][]([DONT\_PARSE] [PREFIX {prefix}] [STRIP prefix\_to\_strip] {path}) <a name="macro_RESOURCE_FILES"></a>
This macro expands into
RESOURCE([DONT\_PARSE] {path} resfs/file/{prefix}{path}
    - resfs/src/resfs/file/{prefix}{remove\_prefix(path, prefix\_to\_strip)}={rootrel\_arc\_src(path)}
)

resfs/src/{key} stores a source root (or build root) relative path of the
source of the value of the {key} resource.

resfs/file/{key} stores any value whose source was a file on a filesystem.
resfs/src/resfs/file/{key} must store its path.

DONT\_PARSE disables parsing for source code files (determined by extension)
           Please don't abuse: use separate DONT\_PARSE macro call only for files subject to parsing

This form is for use from other plugins:
RESOURCE\_FILES([DEST {dest}] {path}) expands into RESOURCE({path} resfs/file/{dest})

@see: https://wiki.yandex-team.ru/devtools/commandsandvars/resourcefiles/

###### Macro [RESTRICT\_LICENSES][](ALLOW\_ONLY|DENY LicenseProperty...) <a name="macro_RESTRICT_LICENSES"></a>
Restrict licenses of direct and indirect module dependencies.

ALLOW\_ONLY restriction type requires dependent module to have at leas one license without propertis not listed in restrictions
list.

DENY restriction type forbids dependency on module with no license without any listed propery from the list.

Note: Can be used multiple times on the same module all specified constraints will be checked.
All macro invocation for the same module must use same constraints type (DENY or ALLOW\_ONLY)

###### Macro [RESTRICT\_PATH][] <a name="macro_RESTRICT_PATH"></a>
Not documented yet.

###### Macro [RUN][] <a name="macro_RUN"></a>
Not documented yet.

###### Macro [RUN\_ANTLR][](Args...) <a name="macro_RUN_ANTLR"></a>
Macro to invoke ANTLR3 generator (general case)

###### Macro [RUN\_ANTLR4][](Args...) <a name="macro_RUN_ANTLR4"></a>
Macro to invoke ANTLR4 generator (general case)

###### Macro [RUN\_ANTLR4\_CPP][](GRAMMAR, OUTPUT\_INCLUDES, LISTENER, VISITOR, Args...) <a name="macro_RUN_ANTLR4_CPP"></a>
Macro to invoke ANTLR4 generator (Cpp)

###### Macro [RUN\_ANTLR4\_GO][](GRAMMAR, DEPS <extra\_go\_deps>, LISTENER, VISITOR, Args...) <a name="macro_RUN_ANTLR4_GO"></a>
Macro to invoke ANTLR4 generator (Go)

###### Macro [RUN\_ANTLR4\_PYTHON][](Grammar [LISTENER] [VISITOR] [SUBDIR] [EXTRA\_OUTS Outs...] Args...) <a name="macro_RUN_ANTLR4_PYTHON"></a>
`LISTENER` - emit grammar listener
`VISITOR` -  emit grammar visitor
`SUBDIR` - place generated files to specified subdirectory of BINDIR
`EXTRA\_OUTS` - list extra outputs produced by Antlr (e.g. .interp and .token files) if they are needed. If `SUBDIR` is specied it will affect these as well. Use file names only.

Macro to invoke ANTLR4 generator (Python). The Python3 will be used for PY3\_LIBRARY/PY3\_PROGRAM/PY3TEST, Python2 will be used in all other cases.

###### Macro [RUN\_JAVA\_PROGRAM][](Args...) <a name="macro_RUN_JAVA_PROGRAM"></a>
Not documented yet.

###### Macro [RUN\_LUA][](script\_path args... [CWD dir] [ENV key=value...] [TOOL tools...] [IN[\_NOPARSE] inputs...] [OUT[\_NOAUTO] outputs...] [STDOUT[\_NOAUTO] output] [OUTPUT\_INCLUDES output\_includes...] [INDUCED\_DEPS $VARs...]) <a name="macro_RUN_LUA"></a>
Run a lua script.
These macros are similar: RUN\_PROGRAM, RUN\_LUA, PYTHON.

Parameters:
- script\_path - Path to the script.3
- args... - Program arguments. Relative paths listed in TOOL, IN, OUT, STDOUT become absolute.
- CWD dir - Absolute path of the working directory.
- ENV key=value... - Environment variables.
- TOOL tools... - Auxiliary tool directories.
- IN[\_NOPARSE] inputs... - Input files. NOPARSE inputs are treated as textual and not parsed for dependencies regardless of file extensions.
- OUT[\_NOAUTO] outputs... - Output files. NOAUTO outputs are not automatically added to the build process.
- STDOUT[\_NOAUTO] output - Redirect the standard output to the output file.
- OUTPUT\_INCLUDES output\_includes... - Includes of the output files that are needed to build them.
- INDUCED\_DEPS $VARs... - Dependencies for generated files. Unlike `OUTPUT\_INCLUDES` these may target files further in processing chain.
                          In order to do so VAR should be filled by PREPARE\_INDUCED\_DEPS macro, stating target files (by type) and set of dependencies

For absolute paths use ${ARCADIA\_ROOT} and ${ARCADIA\_BUILD\_ROOT}, or
${CURDIR} and ${BINDIR} which are expanded where the outputs are used.

###### Macro [RUN\_PROGRAM][](tool\_path args... [CWD dir] [ENV key=value...] [TOOL tools...] [IN[\_NOPARSE] inputs...] [OUT[\_NOAUTO] outputs...] [STDOUT[\_NOAUTO] output] [OUTPUT\_INCLUDES output\_includes...] [INDUCED\_DEPS $VARs...]) <a name="macro_RUN_PROGRAM"></a>
Run a program from arcadia.
These macros are similar: RUN\_PROGRAM, RUN\_LUA, PYTHON.

Parameters:
- tool\_path - Path to the directory of the tool.
- args... - Program arguments. Relative paths listed in TOOL, IN, OUT, STDOUT become absolute.
- CWD dir - Absolute path of the working directory.
- ENV key=value... - Environment variables.
- TOOL tools... - Auxiliary tool directories.
- IN[\_NOPARSE] inputs... - Input files. NOPARSE inputs are treated as textual and not parsed for dependencies regardless of file extensions.
- OUT[\_NOAUTO] outputs... - Output files. NOAUTO outputs are not automatically added to the build process.
- STDOUT[\_NOAUTO] output - Redirect the standard output to the output file.
- OUTPUT\_INCLUDES output\_includes... - Includes of the output files that are needed to build them.
- INDUCED\_DEPS $VARs... - Dependencies for generated files. Unlike `OUTPUT\_INCLUDES` these may target files further in processing chain.
                          In order to do so VAR should be filled by PREPARE\_INDUCED\_DEPS macro, stating target files (by type) and set of dependencies

For absolute paths use ${ARCADIA\_ROOT} and ${ARCADIA\_BUILD\_ROOT}, or
${CURDIR} and ${BINDIR} which are expanded where the outputs are used.
Note that Tool is always built for the host platform, so be careful to provide that tool can be built for all Arcadia major host platforms (Linux, MacOS and Windows).

###### Macro [RUN\_PYTHON3][](script\_path args... [CWD dir] [ENV key=value...] [TOOL tools...] [IN[\_NOPARSE] inputs...] [OUT[\_NOAUTO] outputs...] [STDOUT[\_NOAUTO] output] [OUTPUT\_INCLUDES output\_includes...] [INDUCED\_DEPS $VARs...]) <a name="macro_RUN_PYTHON3"></a>
Run a python script with prebuilt python3 interpretor built from devtools/huge\_python3.
These macros are similar: RUN\_PROGRAM, RUN\_LUA, PYTHON.

Parameters:
- script\_path - Path to the script.
- args... - Program arguments. Relative paths listed in TOOL, IN, OUT, STDOUT become absolute.
- CWD dir - Absolute path of the working directory.
- ENV key=value... - Environment variables.
- TOOL tools... - Auxiliary tool directories.
- IN[\_NOPARSE] inputs... - Input files. NOPARSE inputs are treated as textual and not parsed for dependencies regardless of file extensions.
- OUT[\_NOAUTO] outputs... - Output files. NOAUTO outputs are not automatically added to the build process.
- STDOUT[\_NOAUTO] output - Redirect the standard output to the output file.
- OUTPUT\_INCLUDES output\_includes... - Includes of the output files that are needed to build them.
- INDUCED\_DEPS $VARs... - Dependencies for generated files. Unlike `OUTPUT\_INCLUDES` these may target files further in processing chain.
                          In order to do so VAR should be filled by PREPARE\_INDUCED\_DEPS macro, stating target files (by type) and set of dependencies

For absolute paths use ${ARCADIA\_ROOT} and ${ARCADIA\_BUILD\_ROOT}, or
${CURDIR} and ${BINDIR} which are expanded where the outputs are used.

###### Macro [SDBUS\_CPP\_ADAPTOR][](File) <a name="macro_SDBUS_CPP_ADAPTOR"></a>
Not documented yet.

###### Macro [SDBUS\_CPP\_PROXY][](File) <a name="macro_SDBUS_CPP_PROXY"></a>
Not documented yet.

###### Macro [SECONDARY\_OUTPUT][](filename) _# internal_ <a name="macro_SECONDARY_OUTPUT"></a>
The use of this macro is strictly prohibited!!!

###### Macro [SET][](varname value)  _#builtin_ <a name="macro_SET"></a>
Sets varname to value

###### Macro [SETUP\_EXECTEST][] <a name="macro_SETUP_EXECTEST"></a>
Not documented yet.

###### Macro [SETUP\_PYTEST\_BIN][] <a name="macro_SETUP_PYTEST_BIN"></a>
Not documented yet.

###### Macro [SETUP\_RUN\_PYTHON][] <a name="macro_SETUP_RUN_PYTHON"></a>
Not documented yet.

###### Macro [SET\_APPEND][](varname appendvalue)  _#builtin_ <a name="macro_SET_APPEND"></a>
Appends appendvalue to varname's value using space as a separator

###### Macro [SET\_APPEND\_WITH\_GLOBAL][](varname appendvalue)  _#builtin_ <a name="macro_SET_APPEND_WITH_GLOBAL"></a>
Appends appendvalue to varname's value using space as a separator.
New value is propagated to dependants

###### Macro [SET\_COMPILE\_OUTPUTS\_MODIFIERS][](NOREL?";norel":"") <a name="macro_SET_COMPILE_OUTPUTS_MODIFIERS"></a>
Not documented yet.

###### Macro [SET\_RESOURCE\_MAP\_FROM\_JSON][](VarName, FileName) <a name="macro_SET_RESOURCE_MAP_FROM_JSON"></a>
Loads the platform to resource uri mapping from the json file FileName and assign it to the variable VarName.
'VarName' value format is the same as an input of the DECLARE\_EXTERNAL\_HOST\_RESOURCES\_BUNDLE macro and can be passed to this macro as is.
File 'FileName' contains json with a 'canonized platform -> resource uri' mapping.
The mapping file format see in SET\_RESOURCE\_URI\_FROM\_JSON description.

###### Macro [SET\_RESOURCE\_URI\_FROM\_JSON][](VarName, FileName) <a name="macro_SET_RESOURCE_URI_FROM_JSON"></a>
Assigns a resource uri matched with a current target platform to the variable VarName.
The 'platform to resource uri' mapping is loaded from json file 'FileName'. File content example:
{
    "by\_platform": {
        "linux": {
            "uri": "sbr:12345"
        },
        "darwin": {
            "uri": "sbr:54321"
        }
    }
}

###### Macro [SIZE][](SMALL/MEDIUM/LARGE) <a name="macro_SIZE"></a>
Set the 'size' for the test. Each 'size' has own set of resrtictions, SMALL bein the most restricted and LARGE being the list.
See documentation on test system for more details.

Documentation about the system test: https://wiki.yandex-team.ru/yatool/test/

###### Macro [SKIP\_TEST][](Reason) <a name="macro_SKIP_TEST"></a>
Skip the suite defined by test module. Provide a reason to be output in test execution report.

###### Macro [SOURCE\_GROUP][](...)  _#builtin, deprecated_ <a name="macro_SOURCE_GROUP"></a>
Ignored

###### Macro [SPLIT\_CODEGEN][](tool prefix opts... [OUT\_NUM num] [OUTPUT\_INCLUDES output\_includes...]) <a name="macro_SPLIT_CODEGEN"></a>
Generator of a certain number of parts of the .cpp file + one header .h file from .in

Supports keywords:
1. OUT\_NUM <the number of generated Prefix.N.cpp default 25 (N varies from 0 to 24)>
2. OUTPUT\_INCLUDES <path to files that will be included in generalnyj of macro files>

###### Macro [SPLIT\_DWARF][]() <a name="macro_SPLIT_DWARF"></a>
Emit debug info for the PROGRAM/DLL as a separate file <module\_name>.debug.
NB: It does not help you to save process RSS but can add problems (see e.g. BEGEMOT-2147).

###### Macro [SPLIT\_FACTOR][](x) <a name="macro_SPLIT_FACTOR"></a>
Sets the number of chunks for parallel run tests when used in test module with FORK\_TESTS() or FORK\_SUBTESTS().
If none of those is specified this macro implies FORK\_TESTS().

Supports C++ ut and PyTest.

Documentation about the system test: https://wiki.yandex-team.ru/yatool/test/

###### Macro [SRC][](File Flags...) <a name="macro_SRC"></a>
Compile single file with extra Flags.
Compilation is driven by the last extension of the File and Flags are specific to corresponding compilation command

###### Macro [SRCDIR][](dirlist)  _# builtin_ <a name="macro_SRCDIR"></a>
Add the specified directories to the list of those in which the source files will be searched
Available only for arcadia/contrib

###### Macro [SRCS][](<[GLOBAL] File> ...) <a name="macro_SRCS"></a>
Source files of the project. Files are built according to their extension and put int module output or fed to ultimate PROGRAM/DLL depending on GLOBAL presence.
Arcadia Paths from the root and is relative to the project's LIST are supported

GLOBAL marks next file as direct input to link phase of the program/shared library project built into. This prevents symbols of the file to be excluded by linker as unused.
The scope of the GLOBAL keyword is the following file (that is, in the case of SRCS(GLOBAL foo.cpp bar.cpp) global will be only foo.cpp)

@example:

    LIBRARY(test_global)
        SRCS(GLOBAL foo.cpp)
    END()

This will produce foo.o and feed it to any PROGRAM/DLL module transitively depending on test\_global library. The library itself will be empty and won't produce .a file.

###### Macro [SRC\_C\_AVX][] <a name="macro_SRC_C_AVX"></a>
@uasge SRC\_C\_AVX(File Flags...)

Compile a single C/C++ file with AVX and additional Flags

###### Macro [SRC\_C\_AVX2][] <a name="macro_SRC_C_AVX2"></a>
@uasge SRC\_C\_AVX2(File Flags...)

Compile a single C/C++ file with AVX2 and additional Flags

###### Macro [SRC\_C\_AVX512][] <a name="macro_SRC_C_AVX512"></a>
@uasge SRC\_C\_AVX512(File Flags...)

Compile a single C/C++ file with AVX512 and additional Flags

###### Macro [SRC\_C\_NO\_LTO][] <a name="macro_SRC_C_NO_LTO"></a>
@uasge SRC\_C\_NO\_LTO(File Flags...)

Compile a single C/C++ file with link-time-optimization disabling and additional Flags

###### Macro [SRC\_C\_PCLMUL][] <a name="macro_SRC_C_PCLMUL"></a>
@uasge SRC\_C\_PCLMUL(File Flags...)

Compile a single C/C++ file with PCLMUL and additional Flags

###### Macro [SRC\_C\_PIC][] <a name="macro_SRC_C_PIC"></a>
@uasge SRC\_C\_PIC(File Flags...)

Compile a single C/C++ file with -fPIC and additional Flags

###### Macro [SRC\_C\_SSE2][] <a name="macro_SRC_C_SSE2"></a>
@uasge SRC\_C\_SSE2(File Flags...)

Compile a single C/C++ file with SSE2 and additional Flags

###### Macro [SRC\_C\_SSE3][] <a name="macro_SRC_C_SSE3"></a>
@uasge SRC\_C\_SSE3(File Flags...)

Compile a single C/C++ file with SSE3 and additional Flags

###### Macro [SRC\_C\_SSE4][] <a name="macro_SRC_C_SSE4"></a>
@uasge SRC\_C\_SSE4(File Flags...)

Compile a single C/C++ file with SSE4 and additional Flags

###### Macro [SRC\_C\_SSE41][] <a name="macro_SRC_C_SSE41"></a>
@uasge SRC\_C\_SSE41(File Flags...)

Compile a single C/C++ file with SSE4.1 and additional Flags

###### Macro [SRC\_C\_SSSE3][] <a name="macro_SRC_C_SSSE3"></a>
@uasge SRC\_C\_SSSE3(File Flags...)

Compile a single C/C++ file with SSSE3 and additional Flags

###### Macro [SRC\_C\_XOP][] <a name="macro_SRC_C_XOP"></a>
@uasge SRC\_C\_XOP(File Flags...)

Compile a single C/C++ file with (an AMD-specific instruction set,
see https://en.wikipedia.org/wiki/XOP\_instruction\_set) and additional Flags

###### Macro [SRC\_RESOURCE][](Id) <a name="macro_SRC_RESOURCE"></a>
Not documented yet.

###### Macro [STRIP][]() <a name="macro_STRIP"></a>
Strip debug info from a PROGRAM, DLL or TEST.
This macro doesn't work in LIBRARY's, UNION's and PACKAGE's.

###### Macro [STRUCT\_CODEGEN][](Prefix) <a name="macro_STRUCT_CODEGEN"></a>
A special case BASE\_CODEGEN, in which the kernel/struct\_codegen/codegen\_tool tool is used.

###### Macro [STYLE][](Globs...) <a name="macro_STYLE"></a>
Not documented yet.

###### Macro [STYLE\_PYTHON][]() <a name="macro_STYLE_PYTHON"></a>
Check python3 sources for style issues using black.

###### Macro [SUBSCRIBER][](subscribers...)  _# builtin_ <a name="macro_SUBSCRIBER"></a>
Add observers of the code.
In the SUBSCRIBER macro you can use:
1. login-s from staff.yandex-team.ru
2. Review group (to specify the Code-review group need to use the prefix g:)

Note: current behavior of SUBSCRIBER is almost the same as OWNER. The are only 2 differences: SUBSCRIBER is not mandatory and it may be separately processed by external tools

Ask devtools@yandex-team.ru if you need more information

###### Macro [SUPPRESSIONS][] <a name="macro_SUPPRESSIONS"></a>
SUPPRESSIONS() - allows to specify files with suppression notation which will be used by
address, leak or thread sanitizer runtime by default.
Use asan.supp filename for address sanitizer, lsan.supp for leak sanitizer
and tsan.supp for thread sanitizer suppressions respectively.
See https://clang.llvm.org/docs/AddressSanitizer.html#suppressing-memory-leaks
for details.

###### Macro [SYMLINK][](from to) <a name="macro_SYMLINK"></a>
Add symlink

###### Macro [SYSTEM\_PROPERTIES][]([<Key Value>...] [<File Path>...]) <a name="macro_SYSTEM_PROPERTIES"></a>
List of Key,Value pairs that will be available to test via System.getProperty().
FILE means that parst should be read from file specifies as Path.

Documentation: https://wiki.yandex-team.ru/yatool/test/

###### Macro [TAG][] ([tag...]) <a name="macro_TAG"></a>
Each test can have one or more tags used to filter tests list for running.
There are also special tags affecting test behaviour, for example ya:external, sb:ssd.

Documentation: https://wiki.yandex-team.ru/yatool/test/#obshhieponjatija

###### Macro [TASKLET][]() <a name="macro_TASKLET"></a>
Not documented yet.

###### Macro [TASKLET\_REG][](Name, Lang, Impl, Includes...) <a name="macro_TASKLET_REG"></a>
Not documented yet.

###### Macro [TASKLET\_REG\_EXT][](Name, Lang, Impl, Wrapper, Includes...) <a name="macro_TASKLET_REG_EXT"></a>
Not documented yet.

###### Macro [TEST\_CWD][](path) <a name="macro_TEST_CWD"></a>
Defines working directory for test runs. Often used in conjunction with DATA() macro.
Is only used inside of the TEST modules.

Documentation: https://wiki.yandex-team.ru/yatool/test/

###### Macro [TEST\_DATA][] <a name="macro_TEST_DATA"></a>
Not documented yet.

###### Macro [TEST\_JAVA\_CLASSPATH\_CMD\_TYPE][](Type) <a name="macro_TEST_JAVA_CLASSPATH_CMD_TYPE"></a>
Available types: MANIFEST(default), COMMAND\_FILE, LIST
Method for passing a classpath value to a java command line
MANIFEST via empty jar file with manifest that contains Class-Path attribute
COMMAND\_FILE via @command\_file
LIST via flat args

###### Macro [TEST\_SRCS][](Files...) <a name="macro_TEST_SRCS"></a>
In PY2TEST, PY3TEST and PY\*\_LIBRARY modules used as PY\_SRCS macro and additionally used to mine test cases to be executed by testing framework.

Documentation: https://wiki.yandex-team.ru/yatool/test/#testynapytest

###### Macro [TIMEOUT][](TIMEOUT) <a name="macro_TIMEOUT"></a>
Sets a timeout on test execution

Documentation about the system test: https://wiki.yandex-team.ru/yatool/test/

###### Macro [TOUCH][](Outputs...) _# internal_ <a name="macro_TOUCH"></a>
Just introduce outputs

###### Macro [TS\_TEST\_DATA][]([RENAME] Globs...) <a name="macro_TS_TEST_DATA"></a>
Macro to add tests data (i.e. snapshots) used in testing to a bindir from curdir.
Creates symbolic links to directories of files found by the specified globs.

Parameters:
- RENAME - adds ability to rename paths for tests data from curdir to bindir.
           For example if your tested module located on "module" path and tests data in "module/tests\_data".
           Then you can be able to rename "tests\_data" folder to something else - `RENAME tests\_data:example`.
           As a result in your bindir will be created folder - "module/example" which is a symbolic link on "module/tests\_data" in curdir.
           It is possible to specify multiple renaming rules in the following format "dir1:dir2;dir3/foo:dir4/bar", where "dir1" and "dir3" folders in curdir.
- Globs... - globs to tests data files, symbolic links will be created to their folders. For example - "tests\_data/\*\*/\*".

###### Macro [TS\_TEST\_FOR][](path/to/module)  _#builtin_ <a name="macro_TS_TEST_FOR"></a>
Produces typescript test for specified module

###### Macro [TS\_TEST\_SRCS][](DIRS...) <a name="macro_TS_TEST_SRCS"></a>
Not documented yet.

###### Macro [UBERJAR][]() <a name="macro_UBERJAR"></a>
UBERJAR is a single all-in-one jar-archive that includes all its Java dependencies (reachable PEERDIR).
It also supports shading classes inside the archive by moving them to a different package (similar to the maven-shade-plugin).
Use UBERJAR inside JAVA\_PROGRAM module.

You can use the following macros to configure the archive:
1. UBERJAR\_HIDING\_PREFIX prefix for classes to shade (classes remain in their packages by default)
2. UBERJAR\_HIDE\_EXCLUDE\_PATTERN exclude classes matching this patterns from shading (if enabled).
3. UBERJAR\_PATH\_EXCLUDE\_PREFIX the prefix for classes that should not get into the jar archive (all classes are placed into the archive by default)
4. UBERJAR\_MANIFEST\_TRANSFORMER\_MAIN add ManifestResourceTransformer class to uberjar processing and specify main-class
5. UBERJAR\_MANIFEST\_TRANSFORMER\_ATTRIBUTE add ManifestResourceTransformer class to uberjar processing and specify some attribute
6. UBERJAR\_APPENDING\_TRANSFORMER add AppendingTransformer class to uberjar processing
7. UBERJAR\_SERVICES\_RESOURCE\_TRANSFORMER add ServicesResourceTransformer class to uberjar processing

Documentation: https://wiki.yandex-team.ru/yatool/java/

@see: [JAVA\_PROGRAM](#module\_JAVA\_PROGRAM), [UBERJAR\_HIDING\_PREFIX](#macro\_UBERJAR\_HIDING\_PREFIX), [UBERJAR\_HIDE\_EXCLUDE\_PATTERN](#macro\_UBERJAR\_HIDE\_EXCLUDE\_PATTERN), [UBERJAR\_PATH\_EXCLUDE\_PREFIX](#macro\_UBERJAR\_PATH\_EXCLUDE\_PREFIX)

###### Macro [UBERJAR\_APPENDING\_TRANSFORMER][](Resource) <a name="macro_UBERJAR_APPENDING_TRANSFORMER"></a>
Add AppendingTransformer for UBERJAR() java programs

Parameters:
- Resource - Resource name

@see: [UBERJAR](#macro\_UBERJAR)

###### Macro [UBERJAR\_HIDE\_EXCLUDE\_PATTERN][](Args...) <a name="macro_UBERJAR_HIDE_EXCLUDE_PATTERN"></a>
Exclude classes matching this patterns from shading (if enabled).
Pattern may contain '\*' and '\*\*' globs.
Shading is enabled for UBERJAR program using UBERJAR\_HIDING\_PREFIX macro. If this macro is not specified all classes are shaded.

@see: [UBERJAR](#macro\_UBERJAR), [UBERJAR\_HIDING\_PREFIX](#macro\_UBERJAR\_HIDING\_PREFIX)

###### Macro [UBERJAR\_HIDING\_PREFIX][](Arg) <a name="macro_UBERJAR_HIDING_PREFIX"></a>
Set prefix for classes to shade. All classes in UBERJAR will be moved into package prefixed with Arg.
Classes remain in their packages by default.

@see: [UBERJAR](#macro\_UBERJAR)

###### Macro [UBERJAR\_MANIFEST\_TRANSFORMER\_ATTRIBUTE][](Key, Value) <a name="macro_UBERJAR_MANIFEST_TRANSFORMER_ATTRIBUTE"></a>
Transform manifest.mf for UBERJAR() java programs, set attribute

@see: [UBERJAR](#macro\_UBERJAR)

###### Macro [UBERJAR\_MANIFEST\_TRANSFORMER\_MAIN][](Main) <a name="macro_UBERJAR_MANIFEST_TRANSFORMER_MAIN"></a>
Transform manifest.mf for UBERJAR() java programs, set main-class attribute

@see: [UBERJAR](#macro\_UBERJAR)

###### Macro [UBERJAR\_PATH\_EXCLUDE\_PREFIX][](Args...) <a name="macro_UBERJAR_PATH_EXCLUDE_PREFIX"></a>
Exclude classes matching this patterns from UBERJAR.
By default all dependencies of UBERJAR program will lend in a .jar archive.

@see: [UBERJAR](#macro\_UBERJAR)

###### Macro [UBERJAR\_SERVICES\_RESOURCE\_TRANSFORMER][]() <a name="macro_UBERJAR_SERVICES_RESOURCE_TRANSFORMER"></a>
Add ServicesResourceTransformer for UBERJAR() java programs

@see: [UBERJAR](#macro\_UBERJAR)

###### Macro [UDF\_NO\_PROBE][]() <a name="macro_UDF_NO_PROBE"></a>
Disable UDF import check at build stage

###### Macro [UPDATE\_VCS\_JAVA\_INFO\_NODEP][](Jar) <a name="macro_UPDATE_VCS_JAVA_INFO_NODEP"></a>
Not documented yet.

###### Macro [USE\_COMMON\_GOOGLE\_APIS][](APIS...) <a name="macro_USE_COMMON_GOOGLE_APIS"></a>
Not documented yet.

###### Macro [USE\_CXX][]() <a name="macro_USE_CXX"></a>
Add dependency on C++ runtime
Note: This macro is inteneded for use in \_GO\_BASE\_UNIT like module when the module is built without C++ runtime by default

###### Macro [USE\_DYNAMIC\_CUDA][]() <a name="macro_USE_DYNAMIC_CUDA"></a>
Enable linking of PROGRAM with dynamic CUDA. By default CUDA uses static linking

###### Macro [USE\_ERROR\_PRONE][]() <a name="macro_USE_ERROR_PRONE"></a>
Use errorprone instead of javac for .java compilation.

###### Macro [USE\_EXT\_PROTO][](peerdir\_tag...) <a name="macro_USE_EXT_PROTO"></a>
Configure module to use proto files from existing PROTO\_LIBRARY module.
Additional PEERDIR tags required to build a module can be passed through
EXTRA\_TAGS vararg parameter.

###### Macro [USE\_JAVALITE][]() <a name="macro_USE_JAVALITE"></a>
Use protobuf-javalite for Java

###### Macro [USE\_LINKER\_GOLD][]() <a name="macro_USE_LINKER_GOLD"></a>
Use gold linker for a program. This doesn't work in libraries

###### Macro [USE\_MODERN\_FLEX][]() <a name="macro_USE_MODERN_FLEX"></a>
Use `contrib/tools/flex` as flex tool. Default is `contrib/tools/flex-old`.
@note: by default no header is emitted. Use `USE\_MODERN\_FLEX\_WITH\_HEADER` to add header emission.

###### Macro [USE\_MODERN\_FLEX\_WITH\_HEADER][](<header\_suffix>) <a name="macro_USE_MODERN_FLEX_WITH_HEADER"></a>
Use `contrib/tools/flex` as flex tool. Default is `contrib/tools/flex-old`.
Additionally emit headers with suffix provided. Header suffix should include extension `.h`.

@example: USE\_MODERN\_FLEX\_WITH\_HEADER(\_lexer.h)

###### Macro [USE\_OLD\_FLEX][]() <a name="macro_USE_OLD_FLEX"></a>
Use `contrib/tools/flex-old` as flex tool. This is current default.

###### Macro [USE\_PERL\_514\_LIB][]() <a name="macro_USE_PERL_514_LIB"></a>
Add dependency on Perl 5.14 to your LIBRARY

###### Macro [USE\_PERL\_LIB][]() <a name="macro_USE_PERL_LIB"></a>
Add dependency on Perl to your LIBRARY

###### Macro [USE\_PLANTUML][]() <a name="macro_USE_PLANTUML"></a>
Use PlantUML plug-in for yfm builder to render UML diagrams into documentation

###### Macro [USE\_PYTHON2][]() <a name="macro_USE_PYTHON2"></a>
This adds Python 2.x runtime library to your LIBRARY and makes it Python2-compatible.
Compatibility means proper PEERDIRs, ADDINCLs and variant selection on PEERDIRs to multimodules.

If you'd like to use #include <Python.h> with Python2 specify USE\_PYTHON2 or better make it PY2\_LIBRARY.
If you'd like to use #include <Python.h> with Python3 specify USE\_PYTHON3 or better make it PY3\_LIBRARY.
If you'd like to use #include <Python.h> with both Python2 and Python3 convert your LIBRARY to PY23\_LIBRARY.

@see: [PY2\_LIBRARY](#module\_PY2\_LIBRARY), [PY3\_LIBRARY](#module\_PY3\_LIBRARY), [PY23\_LIBRARY](#multimodule\_PY23\_LIBRARY)

###### Macro [USE\_PYTHON3][]() <a name="macro_USE_PYTHON3"></a>
This adds Python3 library to your LIBRARY and makes it Python3-compatible.
Compatibility means proper PEERDIRs, ADDINCLs and variant selection on PEERDIRs to multimodules.

If you'd like to use #include <Python.h> with Python3 specify USE\_PYTHON3 or better make it PY3\_LIBRARY.
If you'd like to use #include <Python.h> with Python2 specify USE\_PYTHON2 or better make it PY2\_LIBRARY.
If you'd like to use #include <Python.h> with both Python2 and Python3 convert your LIBRARY to PY23\_LIBRARY.

@see: [PY2\_LIBRARY](#module\_PY2\_LIBRARY), [PY3\_LIBRARY](#module\_PY3\_LIBRARY), [PY23\_LIBRARY](#multimodule\_PY23\_LIBRARY)

###### Macro [USE\_RECIPE][](path [arg1 arg2...]) <a name="macro_USE_RECIPE"></a>
Provides prepared environment via recipe for test.

Documentation: https://wiki.yandex-team.ru/yatool/test/recipes

###### Macro [USE\_SKIFF][]() _#wip, do not use_ <a name="macro_USE_SKIFF"></a>
Use mapreduce/yt/skiff\_proto/plugin for C++

###### Macro [USE\_UTIL][]() <a name="macro_USE_UTIL"></a>
Add dependency on util and C++ runtime
Note: This macro is intended for use in \_GO\_BASE\_UNIT like module when the module is build without util by default

###### Macro [VALIDATE\_DATA\_RESTART][](ext) <a name="macro_VALIDATE_DATA_RESTART"></a>
Change uid for resource validation tests. May be useful when sandbox resource ttl is changed, but test status is cached in CI.
You can change ext to change test's uid. For example VALIDATE\_DATA\_RESTART(X), where is X is current revision.

###### Macro [VERSION][](Args...) <a name="macro_VERSION"></a>
Specify version of a module. Currently unused by build system, only informative.

###### Macro [VISIBILITY][](level) <a name="macro_VISIBILITY"></a>
This macro sets visibility level for symbols compiled for the current module. 'level'
may take only one of the following values: DEFAULT, HIDDEN.

###### Macro [WERROR][]() <a name="macro_WERROR"></a>
Consider warnings as errors in the current module.
In the bright future will be removed, since WERROR is the default.
Priorities: NO\_COMPILER\_WARNINGS > NO\_WERROR > WERROR\_MODE > WERROR.

###### Macro [WHOLE\_ARCHIVE][](dirnames...) _# internal_ <a name="macro_WHOLE_ARCHIVE"></a>
Not documented yet.

###### Macro [WINDOWS\_MANIFEST][](Manifest) <a name="macro_WINDOWS_MANIFEST"></a>
Not documented yet.

###### Macro [WITHOUT\_LICENSE\_TEXTS][]() <a name="macro_WITHOUT_LICENSE_TEXTS"></a>
This macro indicates that the module has no license text

###### Macro [WITH\_DYNAMIC\_LIBS][] <a name="macro_WITH_DYNAMIC_LIBS"></a>
$usage: WITH\_DYNAMIC\_LIBS() # restricted

Include dynamic libraries as extra PROGRAM/DLL outputs

###### Macro [WITH\_GROOVY][]() <a name="macro_WITH_GROOVY"></a>
Compile groovy source code in this java module

###### Macro [WITH\_JDK][]() <a name="macro_WITH_JDK"></a>
Add directory with JDK to JAVA\_PROGRAM output

###### Macro [WITH\_KAPT][]() <a name="macro_WITH_KAPT"></a>
Use kapt for as annotation processor

###### Macro [WITH\_KOTLIN][]() <a name="macro_WITH_KOTLIN"></a>
Compile kotlin source code in this java module

###### Macro [WITH\_KOTLINC\_ALLOPEN][](-flags) <a name="macro_WITH_KOTLINC_ALLOPEN"></a>
Enable allopen kotlin compiler plugin https://kotlinlang.org/docs/all-open-plugin.html

###### Macro [WITH\_KOTLINC\_LOMBOK][](-flags) <a name="macro_WITH_KOTLINC_LOMBOK"></a>
Enable lombok kotlin compiler plugin https://kotlinlang.org/docs/lombok.html

###### Macro [WITH\_KOTLINC\_NOARG][](-flags) <a name="macro_WITH_KOTLINC_NOARG"></a>
Enable noarg kotlin compiler plugin https://kotlinlang.org/docs/no-arg-plugin.html

###### Macro [WITH\_KOTLINC\_SERIALIZATION][]() <a name="macro_WITH_KOTLINC_SERIALIZATION"></a>
Enable serialization kotlin compiler plugin https://kotlinlang.org/docs/serialization.html

###### Macro [XSTYPEMAPS][](Names...) <a name="macro_XSTYPEMAPS"></a>
Not documented yet.

###### Macro [XS\_PROTO][](InputProto Dir Outputs...) _# deprecated_ <a name="macro_XS_PROTO"></a>
Generate Perl code from protobuf.
In order to use this macro one should predict all outputs protoc will emit from input\_proto file and enlist those as outputs.

###### Macro [YABS\_GENERATE\_CONF][] <a name="macro_YABS_GENERATE_CONF"></a>
Not documented yet.

###### Macro [YABS\_GENERATE\_PHANTOM\_CONF\_PATCH][] <a name="macro_YABS_GENERATE_PHANTOM_CONF_PATCH"></a>
Not documented yet.

###### Macro [YABS\_GENERATE\_PHANTOM\_CONF\_TEST\_CHECK][] <a name="macro_YABS_GENERATE_PHANTOM_CONF_TEST_CHECK"></a>
Not documented yet.

###### Macro [YA\_CONF\_JSON][] <a name="macro_YA_CONF_JSON"></a>
Add passed ya.conf.json and all bottle's formula external files to resources
File MUST be arcadia root relative path (without "${ARCADIA\_ROOT}/" prefix).
NOTE:
  An external formula file referenced from ya.conf.json must be passed as an arcadia root relative path and
  should be located in any subdirectory of the ya.conf.json location ("build/" if we consider a production).
  The later restriction prevents problems in selectively checkouted arcadia.

###### Macro [YDL\_DESC\_USE\_BINARY][]() <a name="macro_YDL_DESC_USE_BINARY"></a>
Used in conjunction with BUILD\_YDL\_DESC. When enabled, all generated descriptors are binary.

@example:

    PACKAGE()
        YDL_DESC_USE_BINARY()
        BUILD_YDL_DESC(../types.ydl Event Event.ydld)
    END()

This will generate descriptor Event.ydld in a binary format.

###### Macro [YMAPS\_SPROTO][](ProtoFiles...) _# maps-specific_ <a name="macro_YMAPS_SPROTO"></a>
Maps-specific .proto handling: generate .sproto.h files using maps/libs/sproto/sprotoc.

###### Macro [YP\_PROTO\_YSON][](Files... OUT\_OPTS Opts...) <a name="macro_YP_PROTO_YSON"></a>
Generate .yson.go from .proto using yp/go/yson/internal/proto-yson-gen/cmd/proto-yson-gen

###### Macro [YQL\_ABI\_VERSION][](major minor release)) <a name="macro_YQL_ABI_VERSION"></a>
Specifying the supported ABI for YQL\_UDF.

@see: [YQL\_UDF()](#multimodule\_YQL\_UDF)

###### Macro [YQL\_LAST\_ABI\_VERSION][]() <a name="macro_YQL_LAST_ABI_VERSION"></a>
Use the last ABI for YQL\_UDF

###### Macro [YT\_SPEC][](path1 [path2...]) <a name="macro_YT_SPEC"></a>
Allows you to specify json-files with YT task and operation specs,
which will be used to run test node in the YT.
Test must be marked with ya:yt tag.
Files must be relative to the root of Arcadia.

Documentation: https://wiki.yandex-team.ru/yatool/test/

###### Macro [\_AAR\_CMD\_IMPL][](EXTRA\_INPUTS...) _#internal_ <a name="macro__AAR_CMD_IMPL"></a>
Not documented yet.

###### Macro [\_ADD\_CLASSPATH\_CLASH\_CHECK][] _#internal_ <a name="macro__ADD_CLASSPATH_CLASH_CHECK"></a>
Not documented yet.

###### Macro [\_ADD\_CPP\_PROTO\_OUT][](Suf) _#internal_ <a name="macro__ADD_CPP_PROTO_OUT"></a>
Not documented yet.

###### Macro [\_ADD\_DYNLYB\_SEM][](Libname) _#internal_ <a name="macro__ADD_DYNLYB_SEM"></a>
Not documented yet.

###### Macro [\_ADD\_EXTRA\_FLAGS][]([GENERATE] Args...) _# internal_ <a name="macro__ADD_EXTRA_FLAGS"></a>
Generate prefix = " && set\_property SOURCE ${input:SRC} APPEND PROPERTY COMPILE\_OPTIONS " if Args is not empty

###### Macro [\_ADD\_EXTRA\_FLAGS\_IMPL][]([GENERATE] Args...) _# internal_ <a name="macro__ADD_EXTRA_FLAGS_IMPL"></a>
Generate prefix = " && set\_property SOURCE ${input:SRC} APPEND PROPERTY COMPILE\_OPTIONS " before $Args when GENERATE
is specified in the list of actual arguments

###### Macro [\_ADD\_GEN\_JAVA\_SCRIPT][](Out, Template, Props...) _#internal_ <a name="macro__ADD_GEN_JAVA_SCRIPT"></a>
Not documented yet.

###### Macro [\_ADD\_HIDDEN\_INPUTS][](Inputs...) _#internal_ <a name="macro__ADD_HIDDEN_INPUTS"></a>
Not documented yet.

###### Macro [\_ADD\_JAVA\_STYLE\_CHECKS][] _#internal_ <a name="macro__ADD_JAVA_STYLE_CHECKS"></a>
Not documented yet.

###### Macro [\_ADD\_KOTLIN\_STYLE\_CHECKS][] _#internal_ <a name="macro__ADD_KOTLIN_STYLE_CHECKS"></a>
ktlint can be disabled using NO\_LINT() and NO\_LINT(ktlint)

###### Macro [\_ADD\_OPTS\_IF\_NON\_EMPTY][](Opt, Args...) _#internal_ <a name="macro__ADD_OPTS_IF_NON_EMPTY"></a>
Not documented yet.

###### Macro [\_ADD\_PY\_PROTO\_OUT][](Suf) _#internal_ <a name="macro__ADD_PY_PROTO_OUT"></a>
Not documented yet.

###### Macro [\_ADD\_SCU\_NAME][](KV\_VAL) _#internal_ <a name="macro__ADD_SCU_NAME"></a>
Not documented yet.

###### Macro [\_ADD\_YQL\_UDF\_DEPS][]() _#internal_ <a name="macro__ADD_YQL_UDF_DEPS"></a>
Add all needed PEERDIRs to a YQL\_UDF.

https://yql.yandex-team.ru/docs/yt/udf/cpp/

###### Macro [\_ALL\_PY\_SRCS2][](TOP\_LEVEL?"TOP\_LEVEL":"", RECURSIVE?"/\*\*":"", ONLY\_TEST\_FILES?"test\_\*.py":"\*.py", ONLY\_TEST\_FILES2?"\*\_test.py":"\*\*\*", NO\_TEST\_FILES?"\*\*/test\_\*.py \*\*/\*\_test.py":"", NAMESPACE[], REST[], REST2[], EAT\_TAIL[]) _#internal_ <a name="macro__ALL_PY_SRCS2"></a>
Not documented yet.

###### Macro [\_APPEND\_DOCS\_DIR\_FLAG][](DIR, NAMESPACE, DYMMY...) _#internal_ <a name="macro__APPEND_DOCS_DIR_FLAG"></a>
Not documented yet.

###### Macro [\_ARCADIA\_PYTHON3\_ADDINCL][]()  _# internal_ <a name="macro__ARCADIA_PYTHON3_ADDINCL"></a>
This macro sets up Python3 headers for modules with Arcadia python (e.g. PY3\_LIBRARY) and configures module as Python 3.x.

###### Macro [\_ARCADIA\_PYTHON\_ADDINCL][]()  _# internal_ <a name="macro__ARCADIA_PYTHON_ADDINCL"></a>
This macro sets up Python headers for modules with Arcadia python (e.g. PY2\_LIBRARY) and configures module as Python 2.x.

###### Macro [\_ARCHIVE\_SEM\_HELPER][](OUT, DONTCOMPRESS, Files...) _#internal_ <a name="macro__ARCHIVE_SEM_HELPER"></a>
Not documented yet.

###### Macro [\_ARF\_HELPER][] _#internal_ <a name="macro__ARF_HELPER"></a>
This is to join $ALL\_RES\_ and $EXT

###### Macro [\_BARE\_LINK\_MODULE][]() _# internal_ <a name="macro__BARE_LINK_MODULE"></a>
Remove unwanted dependencies for "empty" link module

###### Macro [\_BARE\_MODULE][]() _# internal_ <a name="macro__BARE_MODULE"></a>
Remove unwanted dependencies for "empty" library module

###### Macro [\_BUILDWITH\_CYTHON\_CPP\_DEP][](Src Dep Options...) _# internal_ <a name="macro__BUILDWITH_CYTHON_CPP_DEP"></a>
Generates .cpp file from .pyx and attach extra input Dep.
If Dep changes the .cpp file will be re-generated.

###### Macro [\_BUILDWITH\_CYTHON\_CPP\_H][](Src Dep Options...) _# internal_ <a name="macro__BUILDWITH_CYTHON_CPP_H"></a>
BUILDWITH\_CYTHON\_CPP without .pyx infix and with cdef public .h file.

###### Macro [\_BUILDWITH\_CYTHON\_C\_API\_H][](Src Dep Options...) _# internal_ <a name="macro__BUILDWITH_CYTHON_C_API_H"></a>
BUILDWITH\_CYTHON\_C\_H with cdef api \_api.h file.

###### Macro [\_BUILDWITH\_CYTHON\_C\_DEP][](Src Dep Options...) _# internal_ <a name="macro__BUILDWITH_CYTHON_C_DEP"></a>
Generates .c file from .pyx and attach extra input Dep.
If Dep changes the .c file will be re-generated.

###### Macro [\_BUILDWITH\_CYTHON\_C\_H][](Src Dep Options...) _# internal_ <a name="macro__BUILDWITH_CYTHON_C_H"></a>
BUILDWITH\_CYTHON\_C without .pyx infix and with cdef public .h file.

###### Macro [\_BUILD\_MNS\_CPP][](NAME="", CHECK?, RANKING\_SUFFIX="", Files...) _#internal_ <a name="macro__BUILD_MNS_CPP"></a>
Not documented yet.

###### Macro [\_BUILD\_MNS\_FILE][](Input, Name, Output, Suffix, Check, Fml\_tool, AsmDataName) _#internal_ <a name="macro__BUILD_MNS_FILE"></a>
Not documented yet.

###### Macro [\_BUILD\_MNS\_FILES][] _#internal_ <a name="macro__BUILD_MNS_FILES"></a>
Not documented yet.

###### Macro [\_BUILD\_MNS\_HEADER][](NAME="", CHECK?, RANKING\_SUFFIX="", Files...) _#internal_ <a name="macro__BUILD_MNS_HEADER"></a>
Not documented yet.

###### Macro [\_BUNDLE\_TARGET][](Target, Destination) _#internal_ <a name="macro__BUNDLE_TARGET"></a>
Not documented yet.

###### Macro [\_CHECK\_JAVA\_SRCDIR][] _#internal_ <a name="macro__CHECK_JAVA_SRCDIR"></a>
Not documented yet.

###### Macro [\_CHECK\_RUN\_JAVA\_PROG\_CLASSPATH][] _#internal_ <a name="macro__CHECK_RUN_JAVA_PROG_CLASSPATH"></a>
Not documented yet.

###### Macro [\_COMPILE\_ASRC\_IMPL][](EXTRA\_INPUTS...) _#internal_ <a name="macro__COMPILE_ASRC_IMPL"></a>
Not documented yet.

###### Macro [\_CONDITIONAL\_SRCS][]([USE\_CONDITIONAL\_SRCS] Files...) _# internal_ <a name="macro__CONDITIONAL_SRCS"></a>
Adds Files... to SRCS if first word is `USE\_CONDITIONAL\_SRCS`
To be used with some variable which is set to `USE\_CONDITIONAL\_SRCS` under condition

###### Macro [\_COPY\_FILES\_TO\_BUILD\_PREFIX][] _#internal_ <a name="macro__COPY_FILES_TO_BUILD_PREFIX"></a>
Not documented yet.

###### Macro [\_COPY\_FILE\_IMPL][](FILE, AUTO\_DST="", NOAUTO\_DST="", OUTPUT\_INCLUDES[], INDUCED\_DEPS[]) _#internal_ <a name="macro__COPY_FILE_IMPL"></a>
Not documented yet.

###### Macro [\_CPP\_CFGPROTO\_CMD][](File) _#internal_ <a name="macro__CPP_CFGPROTO_CMD"></a>
Not documented yet.

###### Macro [\_CPP\_EVLOG\_CMD][](File) _#internal_ <a name="macro__CPP_EVLOG_CMD"></a>
Not documented yet.

###### Macro [\_CPP\_FLATC64\_CMD][](SRC, SRCFLAGS...) _#internal_ <a name="macro__CPP_FLATC64_CMD"></a>
Not documented yet.

###### Macro [\_CPP\_FLATC\_CMD][](SRC, SRCFLAGS...) _#internal_ <a name="macro__CPP_FLATC_CMD"></a>
Not documented yet.

###### Macro [\_CPP\_PROTO\_CMD][](File) _#internal_ <a name="macro__CPP_PROTO_CMD"></a>
Not documented yet.

###### Macro [\_CPP\_PROTO\_EVLOG\_CMD][](File) _#internal_ <a name="macro__CPP_PROTO_EVLOG_CMD"></a>
Not documented yet.

###### Macro [\_CPP\_VANILLA\_PROTO\_CMD][](File) _#internal_ <a name="macro__CPP_VANILLA_PROTO_CMD"></a>
Not documented yet.

###### Macro [\_DOCS\_LIBRARY\_CMD\_IMPL][](INCLUDE\_SRCS[], EXTRA\_INPUTS[]) _#internal_ <a name="macro__DOCS_LIBRARY_CMD_IMPL"></a>
Not documented yet.

###### Macro [\_DOCS\_LIBRARY\_EPILOGUE][]() _#internal_ <a name="macro__DOCS_LIBRARY_EPILOGUE"></a>
Not documented yet.

###### Macro [\_DOCS\_MKDOCS\_CMD\_IMPL][](CONFIG, INCLUDE\_SRCS[], EXTRA\_INPUTS[]) _#internal_ <a name="macro__DOCS_MKDOCS_CMD_IMPL"></a>
Not documented yet.

###### Macro [\_DOCS\_SRCS][](SRCDIR=".", EXCLUDE[], INCLUDE...) _#internal_ <a name="macro__DOCS_SRCS"></a>
Not documented yet.

###### Macro [\_DOCS\_YFM\_CMD\_IMPL][](CONFIG, EXTRA\_INPUTS[]) _#internal_ <a name="macro__DOCS_YFM_CMD_IMPL"></a>
Not documented yet.

###### Macro [\_DOCS\_YFM\_USE\_PLANTUML][] _#internal_ <a name="macro__DOCS_YFM_USE_PLANTUML"></a>
\_DOCS\_YFM\_USE\_PLANTUML() # internal

This macr sets appropriate dependencies for use of plantuml plugin

###### Macro [\_DO\_1\_RUN\_JAR\_PROGRAM][](IN\_DIRS\_VAR="uniq", Args...) _#internal_ <a name="macro__DO_1_RUN_JAR_PROGRAM"></a>
Not documented yet.

###### Macro [\_DO\_2\_RUN\_JAR\_PROGRAM][](IN\_DIRS\_VAR="uniq\_", IN\_DIRS\_INPUTS[], IN{input}[], IN\_NOPARSE{input}[], IN\_DIR[], OUT\_NOAUTO{output}[], OUT{output}[], TOOL{tool}[], OUT\_DIR[], CLASSPATH[], ADD\_SRCS\_TO\_CLASSPATH?"yes":"no", CWD="${ARCADIA\_BUILD\_ROOT}", Args...) _#internal_ <a name="macro__DO_2_RUN_JAR_PROGRAM"></a>
Not documented yet.

###### Macro [\_EXPORT\_JAVA\_BINDINGS][](JavaSrcs...) _#internal_ <a name="macro__EXPORT_JAVA_BINDINGS"></a>
Not documented yet.

###### Macro [\_EXPORT\_SWIG\_SOURCES][](SwigSrcs...) _#internal_ <a name="macro__EXPORT_SWIG_SOURCES"></a>
Not documented yet.

###### Macro [\_FAT\_OBJECT\_ARGS\_BASE][](Flag, Lib) _#internal_ <a name="macro__FAT_OBJECT_ARGS_BASE"></a>
Not documented yet.

###### Macro [\_FBS\_NAMESPACE\_IMPL][](NAMESPACE, PATH, DUMMY...) _#internal_ <a name="macro__FBS_NAMESPACE_IMPL"></a>
Not documented yet.

###### Macro [\_FETCH\_CONTRIB][](Id, Out, SBR="sbr:") _#internal_ <a name="macro__FETCH_CONTRIB"></a>
Not documented yet.

###### Macro [\_FILL\_JAR\_COPY\_RESOURCES\_CMD][] _#internal_ <a name="macro__FILL_JAR_COPY_RESOURCES_CMD"></a>
Not documented yet.

###### Macro [\_FILL\_JAR\_GEN\_SRCS][] _#internal_ <a name="macro__FILL_JAR_GEN_SRCS"></a>
Not documented yet.

###### Macro [\_FILTER\_EXTS][](SKIP="", FLAGS...) _#internal_ <a name="macro__FILTER_EXTS"></a>
Not documented yet.

###### Macro [\_FMT\_INDUCED\_DEPS][](For, Deps...) _#internal_ <a name="macro__FMT_INDUCED_DEPS"></a>
Not documented yet.

###### Macro [\_FROM\_EXTERNAL][](ExtFile [AUTOUPDATED script] [RENAME <resource files>] OUT\_[NOAUTO] <output files> [EXECUTABLE])  _#internal_ <a name="macro__FROM_EXTERNAL"></a>
Use resource described as .external file as [FROM\_SANDBOX()](#macro\_FROM\_SANDBOX)/[FROM\_MDS()](#macro\_FROM\_MDS).

###### Macro [\_FROM\_NPM\_LOCKFILES][] _#internal_ <a name="macro__FROM_NPM_LOCKFILES"></a>
Not documented yet.

###### Macro [\_GENERATE\_PY\_EVS\_INTERNAL][](FILES...) _#internal_ <a name="macro__GENERATE_PY_EVS_INTERNAL"></a>
Not documented yet.

###### Macro [\_GENERATE\_PY\_PROTOS\_INTERNAL][](FILES...) _#internal_ <a name="macro__GENERATE_PY_PROTOS_INTERNAL"></a>
Not documented yet.

###### Macro [\_GENTAR\_HELPER][](OUT\_DIR[], Args...) _#internal_ <a name="macro__GENTAR_HELPER"></a>
Not documented yet.

###### Macro [\_GEN\_JAVA\_SCRIPT\_IMPL][](Out, Template, Props...) _#internal_ <a name="macro__GEN_JAVA_SCRIPT_IMPL"></a>
Not documented yet.

###### Macro [\_GLOB][](varname globs...)  _#builtin, internal_ <a name="macro__GLOB"></a>
Sets varname to results of globs application.

In globs are supported:
1. Globstar option: '\*\*' recursively matches directories (allowed once per glob).
2. Wildcard patterns for files and directories with '?' and '\*' special characters.

Note: globs may slow down builds and may match to garbage if extra files present in working copy. Use with care and only if ultimately needed.

###### Macro [\_GO\_COMPILE\_CGO1][](NAME, FLAGS[], FILES...) _#internal_ <a name="macro__GO_COMPILE_CGO1"></a>
Not documented yet.

###### Macro [\_GO\_COMPILE\_CGO2][](NAME, C\_FILES[], S\_FILES[], OBJ\_FILES[], FILES...) _#internal_ <a name="macro__GO_COMPILE_CGO2"></a>
Not documented yet.

###### Macro [\_GO\_COMPILE\_SYMABIS][](FLAGS[], ASM\_FILES...) _#internal_ <a name="macro__GO_COMPILE_SYMABIS"></a>
Not documented yet.

###### Macro [\_GO\_EMBED\_DIR][](PATTERN) _# internal_ <a name="macro__GO_EMBED_DIR"></a>
Define an embed directory DIR.

###### Macro [\_GO\_EMBED\_PATTERN][](PATTERN) _# internal_ <a name="macro__GO_EMBED_PATTERN"></a>
Define an embed pattern.

###### Macro [\_GO\_FLATC\_CMD][](fbs\_file flags...) _# internal_ <a name="macro__GO_FLATC_CMD"></a>
Create a tar archive of .go files generated by flatc for Go. Output tar archive
will have .fbs.gosrc extension. This .fbs.gosrc is specially processed when
--add-protobuf-result flag is specified on the command line for 'ya make ...'
(tar archive is extracted to output directory).

###### Macro [\_GO\_GEN\_COVER\_GO][](GO\_FILE, VAR\_ID) _#internal_ <a name="macro__GO_GEN_COVER_GO"></a>
Not documented yet.

###### Macro [\_GO\_GRPC][]() _#internal_ <a name="macro__GO_GRPC"></a>
Not documented yet.

###### Macro [\_GO\_GRPC\_GATEWAY\_SRCS][](Files...) _#internal_ <a name="macro__GO_GRPC_GATEWAY_SRCS"></a>
Not documented yet.

###### Macro [\_GO\_GRPC\_GATEWAY\_SRCS\_IMPL][](Files...) _#internal_ <a name="macro__GO_GRPC_GATEWAY_SRCS_IMPL"></a>
Not documented yet.

###### Macro [\_GO\_GRPC\_GATEWAY\_SWAGGER\_SRCS][](Files...) _#internal_ <a name="macro__GO_GRPC_GATEWAY_SWAGGER_SRCS"></a>
Not documented yet.

###### Macro [\_GO\_LINK\_EXE\_IMPL][](CGO\_FILES[], EXTRA\_INPUTS[], GO\_FILES...) _#internal_ <a name="macro__GO_LINK_EXE_IMPL"></a>
Not documented yet.

###### Macro [\_GO\_LINK\_LIB\_IMPL][](CGO\_FILES[], EXTRA\_INPUTS[], GO\_FILES...) _#internal_ <a name="macro__GO_LINK_LIB_IMPL"></a>
Not documented yet.

###### Macro [\_GO\_LINK\_TEST\_IMPL][](CGO\_FILES[], EXTRA\_INPUTS[], GO\_TEST\_FILES[], GO\_XTEST\_FILES[], GO\_FILES...) _#internal_ <a name="macro__GO_LINK_TEST_IMPL"></a>
Not documented yet.

###### Macro [\_GO\_PROCESS\_SRCS][] _#internal_ <a name="macro__GO_PROCESS_SRCS"></a>
\_GO\_PROCESS\_SRCS() macro processes only 'CGO' files. All remaining \*.go files
and other input files are currently processed by a link command of the
GO module (GO\_LIBRARY, GO\_PROGRAM)

###### Macro [\_GO\_PROTO\_CMD][](File) _#internal_ <a name="macro__GO_PROTO_CMD"></a>
Not documented yet.

###### Macro [\_GO\_PROTO\_CMD\_IMPL][](File, OPTS...) _#internal_ <a name="macro__GO_PROTO_CMD_IMPL"></a>
Not documented yet.

###### Macro [\_GO\_RESOURCE][] _#internal_ <a name="macro__GO_RESOURCE"></a>
Not documented yet.

###### Macro [\_GO\_SRCS][](Files...) _# internal_ <a name="macro__GO_SRCS"></a>
This macro shouldn't be used in ya.make files, use SRCS() instead.
This is internal macro collecting .go sources for processing within Go modules (GO\_PROGRAM and GO\_LIBRARY)

###### Macro [\_GO\_UNUSED\_SRCS][](FLAGS...) _#internal_ <a name="macro__GO_UNUSED_SRCS"></a>
Not documented yet.

###### Macro [\_HASH\_HELPER][](Args...) _#internal_ <a name="macro__HASH_HELPER"></a>
Not documented yet.

###### Macro [\_INPUT\_WITH\_FLAG][](Flag, IN[]) _#internal_ <a name="macro__INPUT_WITH_FLAG"></a>
Not documented yet.

###### Macro [\_INPUT\_WITH\_FLAG\_IMPL][](IN{input}[], Args...) _#internal_ <a name="macro__INPUT_WITH_FLAG_IMPL"></a>
Not documented yet.

###### Macro [\_IOS\_ASSETS][](AssetsDir, Content...) _#internal_ <a name="macro__IOS_ASSETS"></a>
Not documented yet.

###### Macro [\_JAR\_ANN\_PROC\_OPTS][](Classes...) _#internal_ <a name="macro__JAR_ANN_PROC_OPTS"></a>
Not documented yet.

###### Macro [\_JAR\_SRCS][](SRCDIR=".", PACKAGE\_PREFIX="", EXCLUDE[], FILES[], RESOURCES?"yes":"no", Globs...) _#internal_ <a name="macro__JAR_SRCS"></a>
Not documented yet.

###### Macro [\_JAVAC\_RUN\_HELPER][](JAVAC\_CMD\_WITH\_ARGS...) _#internal_ <a name="macro__JAVAC_RUN_HELPER"></a>
Not documented yet.

###### Macro [\_JAVA\_EVLOG\_CMD][](File) _#internal_ <a name="macro__JAVA_EVLOG_CMD"></a>
Not documented yet.

###### Macro [\_JAVA\_FLATC\_CMD][](fbs\_file) _# internal_ <a name="macro__JAVA_FLATC_CMD"></a>
Create a tar archive of .java files generated by flatc for Java. Output tar
acrchive will have .fbs.jsrc extension. Files with .fbs.jsrc extension will
be added to results when --add-flatbuf-result flag is specified on the command
line for 'ya make ...'

###### Macro [\_JAVA\_PROTO\_CMD][](File) _#internal_ <a name="macro__JAVA_PROTO_CMD"></a>
Not documented yet.

###### Macro [\_JAVA\_PROTO\_PLUGIN\_ARGS\_BASE][](Name, Tool, OutParm...) _#internal_ <a name="macro__JAVA_PROTO_PLUGIN_ARGS_BASE"></a>
Not documented yet.

###### Macro [\_JDK\_VERSION\_MACRO\_CHECK][] _#internal_ <a name="macro__JDK_VERSION_MACRO_CHECK"></a>
Not documented yet.

###### Macro [\_JNI\_CPP\_SWIG\_SRCS][](Srcs...) _#internal_ <a name="macro__JNI_CPP_SWIG_SRCS"></a>
Not documented yet.

###### Macro [\_JNI\_JAVA\_SWIG\_SRCS][](Srcs...) _#internal_ <a name="macro__JNI_JAVA_SWIG_SRCS"></a>
Not documented yet.

###### Macro [\_JSRC\_PROXY\_MOBILE\_LIBRARY\_CMD\_IMPL][](EXTRA\_INPUTS...) _#internal_ <a name="macro__JSRC_PROXY_MOBILE_LIBRARY_CMD_IMPL"></a>
Not documented yet.

###### Macro [\_LANG\_CFLAGS][](SRC) _#internal_ <a name="macro__LANG_CFLAGS"></a>
Not documented yet.

###### Macro [\_LUAJIT\_21\_OBJDUMP][](Src, OUT="") _#internal_ <a name="macro__LUAJIT_21_OBJDUMP"></a>
Not documented yet.

###### Macro [\_LUAJIT\_OBJDUMP][](Src, OUT="") _#internal_ <a name="macro__LUAJIT_OBJDUMP"></a>
Not documented yet.

###### Macro [\_MAKE\_YQL\_PYTHON\_UDF\_TEST][]() _#internal_ <a name="macro__MAKE_YQL_PYTHON_UDF_TEST"></a>
Not documented yet.

###### Macro [\_MAKE\_YQL\_UDF][]() _#internal_ <a name="macro__MAKE_YQL_UDF"></a>
Make module definition an YQL UDF: add all needed dependencies, properties and flags

https://yql.yandex-team.ru/docs/yt/udf/cpp/

###### Macro [\_MAPKITIDL\_PROXY][](args...) _# internal_ <a name="macro__MAPKITIDL_PROXY"></a>
Proxy macro for MAPKITIDL which adds PEERDIR to YMAKE resources

###### Macro [\_MARK\_JAVA\_PROG\_WITH\_SOURCES][](Args...) _#internal_ <a name="macro__MARK_JAVA_PROG_WITH_SOURCES"></a>
Not documented yet.

###### Macro [\_MCU\_CONVERT][](Bin) _#internal_ <a name="macro__MCU_CONVERT"></a>
Not documented yet.

###### Macro DOCS\_DIR(path) _# internal_ <a name="macro__MKDOCS_DOCS_DIR"></a>
Not documented yet.

###### Macro [\_MKDOCS\_EPILOGUE][] _#internal_ <a name="macro__MKDOCS_EPILOGUE"></a>
\_MKDOCS\_EPILOOGUE() # internal

This macro executes macros which should be envoked after all user
specified macros in the ya.make file

###### Macro [\_MOBILE\_DLL\_PREREQUISITES\_CMD][](EXTRA\_INPUTS...) _#internal_ <a name="macro__MOBILE_DLL_PREREQUISITES_CMD"></a>
Not documented yet.

###### Macro [\_MOBILE\_LIBRARY\_PREREQUISITES\_CMD][](OUTPUT, EXTRA\_INPUTS...) _#internal_ <a name="macro__MOBILE_LIBRARY_PREREQUISITES_CMD"></a>
Not documented yet.

###### Macro [\_MOBILE\_LIBRARY\_PREREQUISITES\_IMPL][](OUTPUT, EXTRA\_INPUTS...) _#internal_ <a name="macro__MOBILE_LIBRARY_PREREQUISITES_IMPL"></a>
Not documented yet.

###### Macro [\_MOBILE\_TEST\_APK\_CMD\_IMPL][](OUTPUT, EXTRA\_INPUTS...) _#internal_ <a name="macro__MOBILE_TEST_APK_CMD_IMPL"></a>
Not documented yet.

###### Macro [\_MSVC\_FLAGS\_WINDOWS\_IMPL][](target\_platform compiler\_flags) _# internal_ <a name="macro__MSVC_FLAGS_WINDOWS_IMPL"></a>
Add CFLAGS when the firts argument is WINDOWS

###### Macro [\_MX\_BIN\_TO\_INFO][](Src) _#internal_ <a name="macro__MX_BIN_TO_INFO"></a>
Not documented yet.

###### Macro [\_MX\_GEN\_TABLE][](Srcs...) _#internal_ <a name="macro__MX_GEN_TABLE"></a>
Not documented yet.

###### Macro [\_NODE\_MODULES][](IN{input}[], OUT{output}[]) _#internal_ <a name="macro__NODE_MODULES"></a>
Not documented yet.

###### Macro [\_NOOP\_MACRO][](Args...) _#internal_ <a name="macro__NOOP_MACRO"></a>
Not documented yet.

###### Macro [\_ORDER\_ADDINCL][]([BUILD ...] [SOURCE ...] Args...) _# internal_ <a name="macro__ORDER_ADDINCL"></a>
Order and filter ADDINCLs (Args - is intentionally omitted in ADDINCL macro)

###### Macro [\_PACK\_JAR\_HELPER][](Out) _#internal_ <a name="macro__PACK_JAR_HELPER"></a>
Not documented yet.

###### Macro [\_PROTO\_DESC\_CMD][](File) _#internal_ <a name="macro__PROTO_DESC_CMD"></a>
Not documented yet.

###### Macro [\_PROTO\_PLUGIN\_ARGS\_BASE][](Name, Tool, OutParm...) _#internal_ <a name="macro__PROTO_PLUGIN_ARGS_BASE"></a>
Not documented yet.

###### Macro [\_PY3\_COMPILE\_BYTECODE][](SrcX Src) _# internal_ <a name="macro__PY3_COMPILE_BYTECODE"></a>
Compile Python 3.x .py source file into Arcadia binary form suitable for PY3\_PROGRAM

Documentation: https://wiki.yandex-team.ru/devtools/commandsandvars/pysrcs/#makrospyregister

###### Macro [\_PY3\_REGISTER][]() _# internal_ <a name="macro__PY3_REGISTER"></a>
Register Python 3.x module in internal resource file system. Arcadia Python 3.x importer will be retrieve these on import directive

Documentation: https://wiki.yandex-team.ru/devtools/commandsandvars/pysrcs/#makrospyregister

###### Macro \_PYTHON\_ADDINCL()  _# internal_ <a name="macro__PYTHON3_ADDINCL"></a>
This macro sets up Python 3.x headers for both Arcadia and non-Arcadia python.

###### Macro [\_PYTHON\_ADDINCL][]()  _# internal_ <a name="macro__PYTHON_ADDINCL"></a>
This macro sets up Python 2.x headers for both Arcadia and non-Arcadia python.

###### Macro [\_PY\_COMPILE\_BYTECODE][](SrcX Src) _# internal_ <a name="macro__PY_COMPILE_BYTECODE"></a>
Compile Python 2.x .py source file into Arcadia binary form suitable for PY2\_PROGRAM

Documentation: https://wiki.yandex-team.ru/devtools/commandsandvars/pysrcs/#makrospyregister

###### Macro [\_PY\_ENUM\_SERIALIZATION\_TO\_JSON][](File) _#internal_ <a name="macro__PY_ENUM_SERIALIZATION_TO_JSON"></a>
Not documented yet.

###### Macro [\_PY\_ENUM\_SERIALIZATION\_TO\_PY][](File) _#internal_ <a name="macro__PY_ENUM_SERIALIZATION_TO_PY"></a>
Not documented yet.

###### Macro [\_PY\_EVLOG\_CMD][](File) _#internal_ <a name="macro__PY_EVLOG_CMD"></a>
Not documented yet.

###### Macro [\_PY\_EVLOG\_CMD\_BASE][](File, Suf, Args...) _#internal_ <a name="macro__PY_EVLOG_CMD_BASE"></a>
Not documented yet.

###### Macro [\_PY\_EVLOG\_CMD\_INTERNAL][](File) _#internal_ <a name="macro__PY_EVLOG_CMD_INTERNAL"></a>
Not documented yet.

###### Macro [\_PY\_PROGRAM][] _#internal_ <a name="macro__PY_PROGRAM"></a>
Not documented yet.

###### Macro [\_PY\_PROTO\_CMD][](File) _#internal_ <a name="macro__PY_PROTO_CMD"></a>
Not documented yet.

###### Macro [\_PY\_PROTO\_CMD\_BASE][](File, Suf, Args...) _#internal_ <a name="macro__PY_PROTO_CMD_BASE"></a>
Not documented yet.

###### Macro [\_PY\_PROTO\_CMD\_INTERNAL][](File) _#internal_ <a name="macro__PY_PROTO_CMD_INTERNAL"></a>
Not documented yet.

###### Macro [\_PY\_REGISTER][]() _# internal_ <a name="macro__PY_REGISTER"></a>
Register Python 2.x module in internal resource file system. Arcadia Python 2.x importer will be retrieve these on import directive.

Documentation: https://wiki.yandex-team.ru/devtools/commandsandvars/pysrcs/#makrospyregister

###### Macro [\_PY\_SSQLS\_SRC][](EXT, SRC, SRCFLAGS...) _#internal_ <a name="macro__PY_SSQLS_SRC"></a>
Not documented yet.

###### Macro [\_PY\_SSQLS\_SRCS][](Srcs...) _#internal_ <a name="macro__PY_SSQLS_SRCS"></a>
Not documented yet.

###### Macro \_PY\_SSQLS\_SRC("ssqls", SRC, SRCFLAGS...) _#internal_ <a name="macro__PY_SSQLS_SRC____ssqls"></a>
Not documented yet.

###### Macro [\_PY\_TEST][] _#internal_ <a name="macro__PY_TEST"></a>
Not documented yet.

###### Macro [\_RAW\_PROTO\_SRCS][](files...) _# internal_ <a name="macro__RAW_PROTO_SRCS"></a>
\_RAW\_PROTO\_SRCS is a proxy macro to FILES macro which filters out
GLOBAL keyword from the list of files (NOTE! The order of files listed
originally in call to \_RAW\_PROTO\_SRCS() macro is changed in call to
FILES() macro). Currently this macro copies only files with the following
extensions: .proto, .gztproto, .ev

###### Macro [\_REGISTER\_NO\_CHECK\_IMPORTS][] _#internal_ <a name="macro__REGISTER_NO_CHECK_IMPORTS"></a>
Not documented yet.

###### Macro [\_REQUIRE\_EXPLICIT\_LICENSE][](Prefix...) _#internal_ <a name="macro__REQUIRE_EXPLICIT_LICENSE"></a>
Not documented yet.

###### Macro [\_RESOURCE\_SEM][](INPUTS[], KEYS[]) _#internal_ <a name="macro__RESOURCE_SEM"></a>
Not documented yet.

###### Macro [\_RUN\_JAVA][](IN{input}[], IN\_NOPARSE{input}[], OUT{output}[], OUT\_NOAUTO{output}[], OUTPUT\_INCLUDES[], INDUCED\_DEPS[], TOOL[], STDOUT="", STDOUT\_NOAUTO="", CWD="", ENV[], HIDE\_OUTPUT?"stderr2stdout":"stdout2stderr", Args...) _#internal_ <a name="macro__RUN_JAVA"></a>
Not documented yet.

###### Macro [\_RUN\_JBUILD\_PROGRAM][] _#internal_ <a name="macro__RUN_JBUILD_PROGRAM"></a>
Not documented yet.

###### Macro [\_SETUP\_GO\_GRPC\_GATEWAY][]() _#internal_ <a name="macro__SETUP_GO_GRPC_GATEWAY"></a>
Not documented yet.

###### Macro [\_SET\_DOCS\_BIN\_DIR\_FLAG][](NAMESPACE, DUMMY...) _#internal_ <a name="macro__SET_DOCS_BIN_DIR_FLAG"></a>
Not documented yet.

###### Macro [\_SET\_ENV\_FOR\_CUSTOM\_COMMAND][](Args...) _# internal_ <a name="macro__SET_ENV_FOR_CUSTOM_COMMAND"></a>
Generate prefix " ${CMAKE\_COMMAND} -E env " before $Args if Args is not empty

###### Macro \_TARGET\_SOURCES\_FOR\_HEADERS\_IMPL([GENERATE] Args...) _# internal_ <a name="macro__SET_ENV_FOR_CUSTOM_COMMAND_IMPL"></a>
Generate prefix " ${CMAKE\_COMMAND} -E env " before $Args when GENERATE is specified in the list of actual arguments

###### Macro [\_SET\_FIRST\_VALUE][](name args...) _# internal_ <a name="macro__SET_FIRST_VALUE"></a>
This macro sets the value of `name` variable to the value of next argument

###### Macro [\_SPLIT\_CODEGEN\_BASE][](tool prefix OUTS[] OUTPUT\_INCLUDES[]) _# internal_ <a name="macro__SPLIT_CODEGEN_BASE"></a>
Generator of a certain number .the. cpp file + one header .h file from .in.
This is the call of the generator. Python macro SPLIT\_CODEGEN() is defined in order to properly fill command outputs from OUT\_NUM argument.

###### Macro [\_SRC][](Ext Src Flags) _# internal_ <a name="macro__SRC"></a>
Basic building block of extension-based command dispatching
To enable specific extension processing define \_SRC() macro with fixed first argument (Ext).
Internal logic will apply this macro to all files with this Ext listed in SRC/SRCS macros or outputs
of other commands (except ones marked as noauto)

###### Macro [\_SRCS\_NO\_GLOBAL][](files...) _# internal_ <a name="macro__SRCS_NO_GLOBAL"></a>
Proxy macro to SRCS macro which filters out GLOBAL keyword from the list of source files.
Useful for modules like EXTERNAL\_JAVA\_LIBRARY, where GLOBAL keyword cannot be applied properly.
Note: this macro changes order of source files.

###### Macro [\_SRC\_CPP\_CUSTOM\_FLAGS][](SRC, COMPILE\_OUT\_SUFFIX, CUSTOM\_FLAGS...) _#internal_ <a name="macro__SRC_CPP_CUSTOM_FLAGS"></a>
Not documented yet.

###### Macro [\_SRC\_CUSTOM\_C\_CPP][](Ext MacroName File Flags...) _# internal_ <a name="macro__SRC_CUSTOM_C_CPP"></a>
Defenition of generic macro. Report an error that the File with Ext is not
supported by macro MacroName if no appropriate macro specialization is found.

###### Macro \_SRC\_CUSTOM\_C\_CPP(Ext MacroName File Flags...) _# internal_ <a name="macro__SRC_CUSTOM_C_CPP____C"></a>
Specialization of genreric macro \_SRC\_CUSTOM\_C\_CPP which compiles a single Cpp file (with .C extension)

###### Macro \_SRC\_CUSTOM\_C\_CPP(Ext MacroName File Flags...) _# internal_ <a name="macro__SRC_CUSTOM_C_CPP____c"></a>
Specialization of genreric macro \_SRC\_CUSTOM\_C\_CPP which compiles a single C file (with .c extension)

###### Macro \_SRC\_CUSTOM\_C\_CPP(Ext MacroName File Flags...) _# internal_ <a name="macro__SRC_CUSTOM_C_CPP____cc"></a>
Specialization of genreric macro \_SRC\_CUSTOM\_C\_CPP which compiles a single Cpp file (with .cc extension)

###### Macro \_SRC\_CUSTOM\_C\_CPP(Ext MacroName File Flags...) _# internal_ <a name="macro__SRC_CUSTOM_C_CPP____cpp"></a>
Specialization of genreric macro \_SRC\_CUSTOM\_C\_CPP which compiles a single Cpp file (with .cpp extension)

###### Macro \_SRC\_CUSTOM\_C\_CPP(Ext MacroName File Flags...) _# internal_ <a name="macro__SRC_CUSTOM_C_CPP____cxx"></a>
Specialization of genreric macro \_SRC\_CUSTOM\_C\_CPP which compiles a single Cpp file (with .cxx extension)

###### Macro [\_SRC\_C\_CUSTOM\_FLAGS][](SRC, COMPILE\_OUT\_SUFFIX, CUSTOM\_FLAGS...) _#internal_ <a name="macro__SRC_C_CUSTOM_FLAGS"></a>
Not documented yet.

###### Macro [\_SRC\_STRICT\_C\_CPP][](Ext MacroName File Flags...) _# internal_ <a name="macro__SRC_STRICT_C_CPP"></a>
Defenition of generic macro. Report an error that the File with Ext is not
supported by macro MacroName if no appropriate macro specialization is found.

###### Macro \_SRC\_STRICT\_C\_CPP(Ext MacroName File Flags...) _# internal_ <a name="macro__SRC_STRICT_C_CPP____C"></a>
Specialization of genreric macro \_SRC\_STRICT\_C\_CPP which compiles a single Cpp file (with .C extension)

###### Macro \_SRC\_STRICT\_C\_CPP(Ext MacroName File Flags...) _# internal_ <a name="macro__SRC_STRICT_C_CPP____c"></a>
Specialization of genreric macro \_SRC\_STRICT\_C\_CPP which compiles a single C file (with .c extension)

###### Macro \_SRC\_STRICT\_C\_CPP(Ext MacroName File Flags...) _# internal_ <a name="macro__SRC_STRICT_C_CPP____cc"></a>
Specialization of genreric macro \_SRC\_STRICT\_C\_CPP which compiles a single Cpp file (with .cc extension)

###### Macro \_SRC\_STRICT\_C\_CPP(Ext MacroName File Flags...) _# internal_ <a name="macro__SRC_STRICT_C_CPP____cpp"></a>
Specialization of genreric macro \_SRC\_STRICT\_C\_CPP which compiles a single Cpp file (with .cpp extension)

###### Macro \_SRC\_STRICT\_C\_CPP(Ext MacroName File Flags...) _# internal_ <a name="macro__SRC_STRICT_C_CPP____cxx"></a>
Specialization of genreric macro \_SRC\_STRICT\_C\_CPP which compiles a single Cpp file (with .cxx extension)

###### Macro \_SRC("C", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____C"></a>
Not documented yet.

###### Macro \_SRC("S", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____S"></a>
Not documented yet.

###### Macro \_SRC("asm", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____asm"></a>
Not documented yet.

###### Macro \_SRC("asp", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____asp"></a>
Not documented yet.

###### Macro \_SRC("c", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____c"></a>
Not documented yet.

###### Macro \_SRC("cc", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____cc"></a>
Not documented yet.

###### Macro \_SRC("cfgproto", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____cfgproto"></a>
Not documented yet.

###### Macro \_SRC("cpp", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____cpp"></a>
Not documented yet.

###### Macro \_SRC("cu", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____cu"></a>
Not documented yet.

###### Macro \_SRC("cxx", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____cxx"></a>
Not documented yet.

###### Macro \_SRC("ev", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____ev"></a>
Not documented yet.

###### Macro \_SRC("f", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____f"></a>
Not documented yet.

###### Macro \_SRC("fbs", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____fbs"></a>
Not documented yet.

###### Macro \_SRC("fbs64", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____fbs64"></a>
Not documented yet.

###### Macro \_SRC("fml", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____fml"></a>
Not documented yet.

###### Macro \_SRC("fml2", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____fml2"></a>
Not documented yet.

###### Macro \_SRC("fml3", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____fml3"></a>
Not documented yet.

###### Macro \_SRC("gperf", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____gperf"></a>
Not documented yet.

###### Macro \_SRC("gztproto", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____gztproto"></a>
Not documented yet.

###### Macro \_SRC("in", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____in"></a>
Not documented yet.

###### Macro \_SRC("l", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____l"></a>
Not documented yet.

###### Macro \_SRC("lex", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____lex"></a>
Not documented yet.

###### Macro \_SRC("lpp", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____lpp"></a>
Not documented yet.

###### Macro \_SRC("lua", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____lua"></a>
Not documented yet.

###### Macro \_SRC("m", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____m"></a>
Not documented yet.

###### Macro \_SRC("masm", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____masm"></a>
Not documented yet.

###### Macro \_SRC("mm", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____mm"></a>
Not documented yet.

###### Macro \_SRC("pln", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____pln"></a>
Not documented yet.

###### Macro \_SRC("po", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____po"></a>
Not documented yet.

###### Macro \_SRC("proto", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____proto"></a>
Not documented yet.

###### Macro \_SRC("pysrc", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____pysrc"></a>
Not documented yet.

###### Macro \_SRC("pyx", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____pyx"></a>
Not documented yet.

###### Macro \_SRC("rl", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____rl"></a>
Not documented yet.

###### Macro \_SRC("rl5", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____rl5"></a>
Not documented yet.

###### Macro \_SRC("rl6", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____rl6"></a>
Not documented yet.

###### Macro \_SRC("rodata", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____rodata"></a>
Not documented yet.

###### Macro \_SRC("s", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____s"></a>
Not documented yet.

###### Macro \_SRC("s79", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____s79"></a>
Not documented yet.

###### Macro \_SRC("sc", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____sc"></a>
Not documented yet.

###### Macro \_SRC("sfdl", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____sfdl"></a>
Not documented yet.

###### Macro \_SRC("ssqls", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____ssqls"></a>
Not documented yet.

###### Macro \_SRC("storyboard", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____storyboard"></a>
Not documented yet.

###### Macro \_SRC("swg", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____swg"></a>
Not documented yet.

###### Macro \_SRC("xib", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____xib"></a>
Not documented yet.

###### Macro \_SRC("xs", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____xs"></a>
Not documented yet.

###### Macro \_SRC("xsyn", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____xsyn"></a>
Not documented yet.

###### Macro \_SRC("y", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____y"></a>
Not documented yet.

###### Macro \_SRC("yasm", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____yasm"></a>
Not documented yet.

###### Macro \_SRC("ydl", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____ydl"></a>
Not documented yet.

###### Macro \_SRC("ypp", SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC____ypp"></a>
Not documented yet.

###### Macro [\_SRC\_c][](SRC, COMPILE\_OUT\_SUFFIX="", SRCFLAGS...) _#internal_ <a name="macro__SRC_c"></a>
Not documented yet.

###### Macro [\_SRC\_c\_nodeps][](SRC, OUTFILE, INC...) _#internal_ <a name="macro__SRC_c_nodeps"></a>
Not documented yet.

###### Macro [\_SRC\_cpp][](SRC, COMPILE\_OUT\_SUFFIX="", SRCFLAGS...) _#internal_ <a name="macro__SRC_cpp"></a>
Not documented yet.

###### Macro [\_SRC\_lua\_21][](SRC [SRCFLAGS...]) _# internal_ <a name="macro__SRC_lua_21"></a>
Compile LUA source file to object code using LUA 2.1

###### Macro [\_SRC\_m][](SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC_m"></a>
Not documented yet.

###### Macro [\_SRC\_masm][](SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC_masm"></a>
Not documented yet.

###### Macro [\_SRC\_py2src][](SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC_py2src"></a>
Not documented yet.

###### Macro [\_SRC\_py3src][](SRC, SRCFLAGS...) _#internal_ <a name="macro__SRC_py3src"></a>
Not documented yet.

###### Macro [\_SRC\_yasm][](SRC, PREINCLUDES[], SRCFLAGS...) _#internal_ <a name="macro__SRC_yasm"></a>
Not documented yet.

###### Macro [\_SRC\_yasm\_helper][](SRC, PREINCLUDES[], SRCFLAGS...) _#internal_ <a name="macro__SRC_yasm_helper"></a>
Not documented yet.

###### Macro [\_STYLE][] _#internal_ <a name="macro__STYLE"></a>
Not documented yet.

###### Macro [\_SWIG\_PYTHON\_C][](Src, DstSubPrefix) _# internal_ <a name="macro__SWIG_PYTHON_C"></a>
Like \_SWIG\_PYTHON\_CPP but generate DstSubPrefix\_swg.c.

###### Macro [\_SWIG\_PYTHON\_CPP][](Src, DstSubPrefix) _# internal_ <a name="macro__SWIG_PYTHON_CPP"></a>
Run swig on Src to produce DstSubPrefix.py and DstSubPrefix\_swg.cpp that
provides DstSubPrefix\_swg python module.

###### Macro [\_TARGET\_SOURCES\_FOR\_HEADERS][](Args...) _# internal_ <a name="macro__TARGET_SOURCES_FOR_HEADERS"></a>
Generate prefix " && target\_sources PRIVATE " before $Args if Args is not empty

###### Macro [\_TARGET\_SOURCES\_FOR\_HEADERS\_IMPL][]([GENERATE] Args...) _# internal_ <a name="macro__TARGET_SOURCES_FOR_HEADERS_IMPL"></a>
Generate prefix " && target\_sources PRIVATE " before $Args when GENERATE is specified in the list of actual arguments

###### Macro [\_TS\_CONFIGURE][] _#internal_ <a name="macro__TS_CONFIGURE"></a>
Not documented yet.

###### Macro [\_TS\_LIBRARY\_EPILOGUE][] _#internal_ <a name="macro__TS_LIBRARY_EPILOGUE"></a>
\_TS\_LIBRARY\_EPILOGUE() # internal

This macro executes macros which should be invoked after all user specified macros in the ya.make file

###### Macro [\_TS\_TEST\_CONFIGURE][] _#internal_ <a name="macro__TS_TEST_CONFIGURE"></a>
Not documented yet.

###### Macro [\_UNITTEST][] _#internal_ <a name="macro__UNITTEST"></a>
Not documented yet.

###### Macro [\_USE\_LINKER][]() _#internal_ <a name="macro__USE_LINKER"></a>
Not documented yet.

###### Macro [\_USE\_LINKER\_IMPL][](LINKER\_ID...) _#internal_ <a name="macro__USE_LINKER_IMPL"></a>
Not documented yet.

###### Macro [\_XS\_SRCS][](SRC, TYPEMAPS[], SRCFLAGS...) _#internal_ <a name="macro__XS_SRCS"></a>
Not documented yet.

###### Macro [\_YA\_CONF\_JSON][] _#internal_ <a name="macro__YA_CONF_JSON"></a>
Not documented yet.

###### Macro DOCS\_DIR(path) _# internal_ <a name="macro__YFM_DOCS_DIR"></a>
Not documented yet.

###### Macro [\_YMAKE\_GENERATE\_SCRIPT][] _#internal_ <a name="macro__YMAKE_GENERATE_SCRIPT"></a>
Not documented yet.

###### Macro [\_YMAPS\_GENERATE\_SPROTO\_HEADER][](File) _#internal_ <a name="macro__YMAPS_GENERATE_SPROTO_HEADER"></a>
Not documented yet.

###### Macro [\_YTEST][] _#internal_ <a name="macro__YTEST"></a>
Not documented yet.

 [DLL\_JAVA]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/java.ymake.conf?rev=10074629#L193
 [DOCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/docs.conf?rev=10074629#L148
 [DYNAMIC\_LIBRARY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3042
 [FBS\_LIBRARY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8134
 [JAR\_PROGRAM]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3934
 [JAVA\_CONTRIB\_PROGRAM]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/java.ymake.conf?rev=10074629#L147
 [JAVA\_PROGRAM]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/java.ymake.conf?rev=10074629#L32
 [JTEST]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/java.ymake.conf?rev=10074629#L87
 [JTEST\_FOR]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/java.ymake.conf?rev=10074629#L117
 [JTEST\_YMAKE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3985
 [JUNIT5]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/java.ymake.conf?rev=10074629#L58
 [JUNIT5\_YMAKE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3966
 [MAPS\_IDL\_LIBRARY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/mapkit.conf?rev=10074629#L86
 [MKDOCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/docs.conf?rev=10074629#L269
 [PROTO\_LIBRARY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7884
 [PY23\_LIBRARY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9594
 [PY23\_NATIVE\_LIBRARY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9630
 [PY23\_TEST]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9835
 [PY3TEST]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2296
 [PY3\_PROGRAM]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1826
 [SANDBOX\_PY23\_TASK]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5102
 [SANDBOX\_PY3\_TASK]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5150
 [SANDBOX\_TASK]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5077
 [SSQLS\_LIBRARY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9947
 [YQL\_UDF]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/yql_udf.conf?rev=10074629#L103
 [AAR]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/aar.conf?rev=10074629#L312
 [AAR\_PROXY\_LIBRARY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/aar.conf?rev=10074629#L347
 [ASRC\_LIBRARY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/asrc.conf?rev=10074629#L51
 [BOOSTTEST]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2003
 [BOOSTTEST\_WITH\_MAIN]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2023
 [CI\_GROUP]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3171
 [CONTAINER]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9980
 [CONTAINER\_LAYER]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9970
 [CPP\_STYLE\_TEST]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2309
 [CUSTOM\_BUILD\_LIBRARY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9994
 [DEFAULT\_IOS\_INTERFACE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9708
 [DEV\_DLL\_PROXY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2987
 [DLL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2938
 [DLL\_PROXY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3011
 [DLL\_PROXY\_LIBRARY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8242
 [DLL\_TOOL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2955
 [DLL\_UNIT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2717
 [DOCS\_LIBRARY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/docs.conf?rev=10074629#L82
 [EXECTEST]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2362
 [EXTERNAL\_JAVA\_LIBRARY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3292
 [FAT\_OBJECT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2657
 [FUZZ]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1959
 [GO\_DLL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9057
 [GO\_LIBRARY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8958
 [GO\_PROGRAM]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8975
 [GO\_TEST]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9077
 [GTEST]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1939
 [GTEST\_UGLY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2328
 [G\_BENCHMARK]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2391
 [IOS\_INTERFACE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9697
 [JAR\_LIBRARY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3703
 [JAVA\_CONTRIB]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3474
 [JAVA\_CONTRIB\_PROXY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3434
 [JAVA\_LIBRARY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/java.ymake.conf?rev=10074629#L22
 [JSRC\_LIBRARY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8186
 [JSRC\_PROXY\_MOBILE\_LIBRARY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/asrc.conf?rev=10074629#L95
 [LIBRARY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2514
 [MCU\_PROGRAM]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L10052
 [MOBILE\_BOOST\_TEST\_APK]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/aar.conf?rev=10074629#L163
 [MOBILE\_DLL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/aar.conf?rev=10074629#L25
 [MOBILE\_LIBRARY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/asrc.conf?rev=10074629#L81
 [MOBILE\_TEST\_APK]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/aar.conf?rev=10074629#L123
 [NPM\_CONTRIBS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/ts.conf?rev=10074629#L34
 [PACKAGE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3147
 [PREBUILT\_PROGRAM]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8253
 [PROGRAM]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1769
 [PROTO\_DESCRIPTIONS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8091
 [PROTO\_REGISTRY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8103
 [PY2MODULE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2849
 [PY2TEST]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2249
 [PY2\_LIBRARY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4016
 [PY2\_PROGRAM]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1794
 [PY3MODULE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2868
 [PY3TEST\_BIN]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2267
 [PY3\_LIBRARY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4052
 [PY3\_PROGRAM\_BIN]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4200
 [PYTEST\_BIN]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2232
 [PY\_ANY\_MODULE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2796
 [PY\_PACKAGE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3232
 [RECURSIVE\_LIBRARY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2691
 [RESOURCES\_LIBRARY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2591
 [R\_MODULE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2907
 [SO\_PROGRAM]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2967
 [TS\_BUNDLE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/ts.conf?rev=10074629#L162
 [TS\_LIBRARY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/ts.conf?rev=10074629#L135
 [TS\_TEST]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/ts.conf?rev=10074629#L230
 [UDF\_BASE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/yql_udf.conf?rev=10074629#L16
 [UNION]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3207
 [UNITTEST]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1907
 [UNITTEST\_FOR]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2418
 [UNITTEST\_WITH\_CUSTOM\_ENTRY\_POINT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1928
 [YQL\_PYTHON3\_UDF]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/yql_udf.conf?rev=10074629#L198
 [YQL\_PYTHON3\_UDF\_TEST]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/yql_udf.conf?rev=10074629#L246
 [YQL\_PYTHON\_UDF]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/yql_udf.conf?rev=10074629#L147
 [YQL\_PYTHON\_UDF\_PROGRAM]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/yql_udf.conf?rev=10074629#L173
 [YQL\_PYTHON\_UDF\_TEST]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/yql_udf.conf?rev=10074629#L232
 [YQL\_UDF\_MODULE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/yql_udf.conf?rev=10074629#L82
 [YQL\_UDF\_TEST]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/yql_udf.conf?rev=10074629#L38
 [YT\_UNITTEST]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1919
 [Y\_BENCHMARK]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2380
 [\_BARE\_UNIT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1178
 [\_BASE\_PROGRAM]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1697
 [\_BASE\_PY3\_PROGRAM]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4153
 [\_BASE\_PYTEST]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2213
 [\_BASE\_PY\_PROGRAM]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4092
 [\_BASE\_UNIT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1202
 [\_BASE\_UNITTEST]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1889
 [\_COMPILABLE\_JAR\_BASE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3679
 [\_DLL\_COMPATIBLE\_LIBRARY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3109
 [\_DOCS\_BARE\_UNIT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/docs.conf?rev=10074629#L53
 [\_DOCS\_BASE\_UNIT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/docs.conf?rev=10074629#L114
 [\_GO\_BASE\_UNIT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8791
 [\_GO\_DLL\_BASE\_UNIT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9013
 [\_JAR\_BASE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3410
 [\_JAR\_RUNNABLE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3893
 [\_JAR\_TEST]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3953
 [\_JAVA\_PLACEHOLDER]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4936
 [\_LIBRARY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2429
 [\_LINK\_UNIT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1652
 [\_MKDOCS\_BASE\_UNIT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/docs.conf?rev=10074629#L240
 [\_PROXY\_LIBRARY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8210
 [\_PY2\_PROGRAM]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1777
 [\_PY\_PACKAGE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3219
 [\_TS\_BASE\_LIBRARY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/ts.conf?rev=10074629#L111
 [\_TS\_BASE\_UNIT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/ts.conf?rev=10074629#L91
 [\_YQL\_UDF\_PROGRAM\_BASE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/yql_udf.conf?rev=10074629#L88
 [AARS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/aar.conf?rev=10074629#L20
 [AAR\_AARS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/aar.conf?rev=10074629#L194
 [AAR\_AIDL\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/aar.conf?rev=10074629#L207
 [AAR\_ASSETS\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/aar.conf?rev=10074629#L214
 [AAR\_BUNDLES]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/aar.conf?rev=10074629#L221
 [AAR\_COMPILE\_ONLY\_AARS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/aar.conf?rev=10074629#L200
 [AAR\_GRADLE\_SCRIPT\_GENERATOR]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/aar.conf?rev=10074629#L255
 [AAR\_JAVA\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/aar.conf?rev=10074629#L235
 [AAR\_JNI\_LIBS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/aar.conf?rev=10074629#L228
 [AAR\_LOCAL\_MAVEN\_REPO]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/aar.conf?rev=10074629#L249
 [AAR\_MANIFEST]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/aar.conf?rev=10074629#L182
 [AAR\_PROGUARD\_RULES]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/aar.conf?rev=10074629#L188
 [AAR\_RES\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/aar.conf?rev=10074629#L242
 [ACCELEO]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/java.ymake.conf?rev=10074629#L12
 [ADDINCL]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [ADDINCLSELF]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5783
 [ADD\_CHECK]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/ytest.py?rev=10074629#L551
 [ADD\_CHECK\_PY\_IMPORTS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/ytest.py?rev=10074629#L668
 [ADD\_CLANG\_TIDY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1685
 [ADD\_COMPILABLE\_TRANSLATE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5449
 [ADD\_COMPILABLE\_TRANSLIT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5459
 [ADD\_DLLS\_TO\_JAR]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4782
 [ADD\_PERL\_MODULE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5338
 [ADD\_PYTEST\_BIN]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/ytest.py?rev=10074629#L741
 [ADD\_PYTEST\_SCRIPT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/ytest.py?rev=10074629#L712
 [ADD\_YTEST]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/ytest.py?rev=10074629#L421
 [ALLOCATOR]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5368
 [ALL\_PYTEST\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9571
 [ALL\_PY\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9553
 [ALL\_RESOURCE\_FILES]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5544
 [ALL\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3099
 [ANNOTATION\_PROCESSOR]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4737
 [APPHOST]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L10086
 [ARCHIVE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6712
 [ARCHIVE\_ASM]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6690
 [ARCHIVE\_BY\_KEYS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6723
 [ASM\_PREINCLUDE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7722
 [ASSERT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/macros_with_error.py?rev=10074629#L25
 [BASE\_CODEGEN]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6797
 [BISON\_FLAGS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/bison_lex.conf?rev=10074629#L32
 [BISON\_GEN\_C]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/bison_lex.conf?rev=10074629#L39
 [BISON\_GEN\_CPP]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/bison_lex.conf?rev=10074629#L47
 [BISON\_HEADER]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/bison_lex.conf?rev=10074629#L69
 [BISON\_NO\_HEADER]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/bison_lex.conf?rev=10074629#L76
 [BPF]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7595
 [BPF\_STATIC]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7609
 [BUILDWITH\_CYTHON\_C]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6577
 [BUILDWITH\_CYTHON\_CPP]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6546
 [BUILDWITH\_RAGEL6]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6634
 [BUILD\_CATBOOST]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/other.conf?rev=10074629#L9
 [BUILD\_MN]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7131
 [BUILD\_MNS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7156
 [BUILD\_ONLY\_IF]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [BUILD\_YDL\_DESC]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6283
 [BUNDLE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/bundle.py?rev=10074629#L4
 [BUNDLE\_AIDL\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/asrc.conf?rev=10074629#L14
 [BUNDLE\_ASSETS\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/asrc.conf?rev=10074629#L35
 [BUNDLE\_EXTRA\_INPUTS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/asrc.conf?rev=10074629#L8
 [BUNDLE\_JAVA\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/asrc.conf?rev=10074629#L21
 [BUNDLE\_RES\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/asrc.conf?rev=10074629#L28
 [CFG\_VARS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6780
 [CFLAGS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6847
 [CGO\_CFLAGS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8583
 [CGO\_LDFLAGS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8592
 [CGO\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8566
 [CHECK\_ALLOWED\_PATH]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/container_layers.py?rev=10074629#L3
 [CHECK\_CONFIG\_H]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L504
 [CHECK\_CONTRIB\_CREDITS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/credits.py?rev=10074629#L8
 [CHECK\_DEPENDENT\_DIRS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L538
 [CHECK\_JAVA\_DEPS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4511
 [CLANG\_EMIT\_AST\_CXX]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7566
 [CLEAN\_TEXTREL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2709
 [CMAKE\_EXPORTED\_TARGET\_NAME]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/opensource.conf?rev=10074629#L61
 [COLLECT\_FRONTEND\_FILES]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9777
 [COLLECT\_JINJA\_TEMPLATES]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8272
 [COLLECT\_YDB\_API\_SPECS\_LEGACY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L10076
 [COMPILE\_C\_AS\_CXX]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7499
 [COMPILE\_LUA]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6225
 [COMPILE\_LUA\_21]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6243
 [COMPILE\_NLG]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7167
 [COMPILE\_SWIFT\_MODULE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9791
 [CONFIGURE\_FILE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6789
 [CONFTEST\_LOAD\_POLICY\_LOCAL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2138
 [CONLYFLAGS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6862
 [COPY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/cp.py?rev=10074629#L6
 [COPY\_FILE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5517
 [COPY\_FILE\_WITH\_CONTEXT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5526
 [CPP\_ADDINCL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7778
 [CPP\_ENUMS\_SERIALIZATION]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/pybuild.py?rev=10074629#L665
 [CPP\_PROTO\_PLUGIN]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L756
 [CPP\_PROTO\_PLUGIN0]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L742
 [CPP\_PROTO\_PLUGIN2]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L767
 [CREATE\_BUILDINFO\_FOR]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6760
 [CREATE\_INIT\_PY\_STRUCTURE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/create_init_py.py?rev=10074629#L6
 [CREDITS\_DISCLAIMER]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/credits.py?rev=10074629#L4
 [CTEMPLATE\_VARNAMES]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7515
 [CUDA\_NVCC\_FLAGS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6876
 [CUSTOM\_LINK\_STEP\_SCRIPT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1882
 [CXXFLAGS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6869
 [DARWIN\_SIGNED\_RESOURCE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9688
 [DARWIN\_STRINGS\_RESOURCE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9684
 [DATA]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2098
 [DEB\_VERSION]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7120
 [DECIMAL\_MD5\_LOWER\_32\_BITS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6772
 [DECLARE\_EXTERNAL\_HOST\_RESOURCES\_BUNDLE]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [DECLARE\_EXTERNAL\_HOST\_RESOURCES\_BUNDLE\_BY\_JSON]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [DECLARE\_EXTERNAL\_HOST\_RESOURCES\_PACK]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [DECLARE\_EXTERNAL\_RESOURCE]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [DECLARE\_EXTERNAL\_RESOURCE\_BY\_JSON]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [DEFAULT]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [DEPENDENCY\_MANAGEMENT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4820
 [DEPENDS]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [DIRECT\_DEPS\_ONLY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4920
 [DISABLE]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [DISABLE\_DATA\_VALIDATION]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2083
 [DLL\_FOR]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [DOCS\_CONFIG]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/docs.conf?rev=10074629#L375
 [DOCS\_COPY\_FILES]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/docs.conf?rev=10074629#L13
 [DOCS\_DIR]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/docs.conf?rev=10074629#L324
 [DOCS\_INCLUDE\_SOURCES]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/docs.conf?rev=10074629#L399
 [DOCS\_VARS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/docs.conf?rev=10074629#L387
 [DUMPERF\_CODEGEN]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6827
 [DYNAMIC\_DEPS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3031
 [DYNAMIC\_LIBRARY\_FROM]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2924
 [ELSE]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [ELSEIF]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [EMBED\_JAVA\_VCS\_INFO]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3282
 [ENABLE]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [ENABLE\_PREVIEW]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4701
 [END]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [ENDIF]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [ENV]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2131
 [EXCLUDE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4746
 [EXCLUDE\_TAGS]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [EXPORTS\_SCRIPT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1850
 [EXPORT\_ALL\_DYNAMIC\_SYMBOLS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1864
 [EXPORT\_MAPKIT\_PROTO]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/mapkit.conf?rev=10074629#L57
 [EXPORT\_YMAPS\_PROTO]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/sproto.conf?rev=10074629#L4
 [EXPOSE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7849
 [EXTERNAL\_JAR]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/java.py?rev=10074629#L256
 [EXTERNAL\_RESOURCE]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [EXTRADIR]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [EXTRALIBS]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [EXTRALIBS\_STATIC]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5442
 [FAT\_RESOURCE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/res.py?rev=10074629#L41
 [FBS\_NAMESPACE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8116
 [FBS\_TO\_PYSRC]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1107
 [FILES]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/files.py?rev=10074629#L1
 [FLATC\_FLAGS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1093
 [FLAT\_JOIN\_SRCS\_GLOBAL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5668
 [FLEX\_FLAGS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/bison_lex.conf?rev=10074629#L25
 [FLEX\_GEN\_C]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/bison_lex.conf?rev=10074629#L55
 [FLEX\_GEN\_CPP]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/bison_lex.conf?rev=10074629#L62
 [FORK\_SUBTESTS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5600
 [FORK\_TESTS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5586
 [FORK\_TEST\_FILES]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5626
 [FROM\_ARCHIVE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7484
 [FROM\_MDS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7454
 [FROM\_NPM]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/ts.conf?rev=10074629#L60
 [FROM\_NPM\_LOCKFILES]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/ts.conf?rev=10074629#L53
 [FROM\_SANDBOX]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7446
 [FUZZ\_DICTS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2035
 [FUZZ\_OPTS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2054
 [GENERATED\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7557
 [GENERATE\_ENUM\_SERIALIZATION]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7099
 [GENERATE\_ENUM\_SERIALIZATION\_WITH\_HEADER]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7111
 [GENERATE\_PY\_PROTOS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5477
 [GENERATE\_SCRIPT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/java.py?rev=10074629#L60
 [GEN\_SCHEEME2]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7247
 [GLOBAL\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3081
 [GOLANG\_VERSION]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8435
 [GO\_ASM\_FLAGS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8397
 [GO\_BENCH\_TIMEOUT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9066
 [GO\_CGO1\_FLAGS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8405
 [GO\_CGO2\_FLAGS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8413
 [GO\_COMPILE\_FLAGS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8421
 [GO\_EMBED\_DIR]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8665
 [GO\_EMBED\_PATTERN]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8629
 [GO\_EMBED\_TEST\_DIR]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8673
 [GO\_EMBED\_XTEST\_DIR]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8681
 [GO\_FAKE\_OUTPUT]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/plugins/plugin_go_fake_output_handler.cpp?rev=10074629#L110
 [GO\_GRPC\_GATEWAY\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8728
 [GO\_GRPC\_GATEWAY\_SWAGGER\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8736
 [GO\_LDFLAGS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8575
 [GO\_LINK\_FLAGS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8429
 [GO\_MOCKGEN\_FROM]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9101
 [GO\_MOCKGEN\_MOCKS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9125
 [GO\_MOCKGEN\_REFLECT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9111
 [GO\_MOCKGEN\_TYPES]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9106
 [GO\_PACKAGE\_NAME]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8521
 [GO\_PROTO\_PLUGIN]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L866
 [GO\_SKIP\_TESTS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8603
 [GO\_TEST\_EMBED\_PATTERN]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8637
 [GO\_TEST\_FOR]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [GO\_TEST\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8540
 [GO\_XTEST\_EMBED\_PATTERN]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8645
 [GO\_XTEST\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8551
 [GRADLE\_FLAGS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/aar.conf?rev=10074629#L6
 [GRPC]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1077
 [IDEA\_EXCLUDE\_DIRS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4662
 [IDEA\_JAR\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3344
 [IDEA\_MODULE\_NAME]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4682
 [IDEA\_RESOURCE\_DIRS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4672
 [IF]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [INCLUDE]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [INCLUDE\_ONCE]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [INCLUDE\_TAGS]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [INDUCED\_DEPS]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [IOS\_APP\_ASSETS\_FLAGS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9680
 [IOS\_APP\_COMMON\_FLAGS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9674
 [IOS\_APP\_SETTINGS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/ios_app_settings.py?rev=10074629#L5
 [IOS\_ASSETS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/ios_assets.py?rev=10074629#L6
 [JAR\_ANNOTATION\_PROCESSOR]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3391
 [JAR\_EXCLUDE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5060
 [JAR\_INCLUDE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5052
 [JAR\_RESOURCE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3454
 [JAVAC\_FLAGS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4691
 [JAVA\_DEPENDENCIES\_CONFIGURATION]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5036
 [JAVA\_EXTERNAL\_DEPENDENCIES]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4929
 [JAVA\_IGNORE\_CLASSPATH\_CLASH\_FOR]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9495
 [JAVA\_MODULE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/java.py?rev=10074629#L77
 [JAVA\_PROTO\_PLUGIN]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L718
 [JAVA\_RESOURCE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3670
 [JAVA\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4776
 [JAVA\_TEST]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/ytest.py?rev=10074629#L809
 [JAVA\_TEST\_DEPS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/ytest.py?rev=10074629#L901
 [JDK\_VERSION]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9745
 [JOIN\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5647
 [JOIN\_SRCS\_GLOBAL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5658
 [JVM\_ARGS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4500
 [KAPT\_ANNOTATION\_PROCESSOR]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3541
 [KAPT\_ANNOTATION\_PROCESSOR\_CLASSPATH]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3548
 [KAPT\_OPTS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3534
 [KOTLINC\_FLAGS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4866
 [LARGE\_FILES]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7475
 [LDFLAGS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6837
 [LICENSE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/license.conf?rev=10074629#L385
 [LICENSE\_TEXTS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L10020
 [LINKER\_SCRIPT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/linker_script.py?rev=10074629#L1
 [LINK\_EXEC\_DYN\_LIB\_IMPL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1644
 [LINK\_EXE\_IMPL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1638
 [LINT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2188
 [LJ\_21\_ARCHIVE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/lj_archive.py?rev=10074629#L23
 [LJ\_ARCHIVE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/lj_archive.py?rev=10074629#L1
 [LLVM\_BC]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/llvm_bc.py?rev=10074629#L6
 [LLVM\_COMPILE\_C]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7585
 [LLVM\_COMPILE\_CXX]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7575
 [LLVM\_COMPILE\_LL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7618
 [LLVM\_LINK]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7627
 [LLVM\_OPT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7637
 [LOCAL\_JAR]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3464
 [LOCAL\_SOURCES\_JAR]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3469
 [MACROS\_WITH\_ERROR]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/macros_with_error.py?rev=10074629#L8
 [MANUAL\_GENERATION]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6012
 [MAPKITIDL]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/plugins/plugin_mapkitidl_handler.cpp?rev=10074629#L412
 [MAPKIT\_ADDINCL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/mapkit.conf?rev=10074629#L2
 [MAPKIT\_ENABLE\_WHOLE\_ARCHIVE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/mapkit.conf?rev=10074629#L76
 [MAPSMOBI\_COLLECT\_AIDL\_FILES]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/mapkit.conf?rev=10074629#L123
 [MAPSMOBI\_COLLECT\_ASSETS\_FILES]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/mapkit.conf?rev=10074629#L115
 [MAPSMOBI\_COLLECT\_JAVA\_FILES]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/mapkit.conf?rev=10074629#L131
 [MAPSMOBI\_COLLECT\_JNI\_LIBS\_FILES]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/mapkit.conf?rev=10074629#L139
 [MAPSMOBI\_COLLECT\_RES\_FILES]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/mapkit.conf?rev=10074629#L147
 [MAPSMOBI\_COLLECT\_TPL\_FILES]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/mapkit.conf?rev=10074629#L155
 [MAPSMOBI\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/mapkit.conf?rev=10074629#L49
 [MAPS\_GARDEN\_COLLECT\_MODULE\_TRAITS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/mapkit.conf?rev=10074629#L163
 [MAPS\_IDL\_ADDINCL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/mapkit.conf?rev=10074629#L10
 [MAPS\_IDL\_GLOBAL\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/mapkit.conf?rev=10074629#L35
 [MAPS\_IDL\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/mapkit.conf?rev=10074629#L28
 [MASMFLAGS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6854
 [MAVEN\_GROUP\_ID]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4726
 [MESSAGE]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [MOBILE\_TEST\_APK\_AAR\_AARS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/aar.conf?rev=10074629#L51
 [MOBILE\_TEST\_APK\_AAR\_BUNDLES]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/aar.conf?rev=10074629#L57
 [MOBILE\_TEST\_APK\_AAR\_MANIFEST]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/aar.conf?rev=10074629#L39
 [MOBILE\_TEST\_APK\_AAR\_PROGUARD\_RULES]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/aar.conf?rev=10074629#L45
 [MOBILE\_TEST\_APK\_TEMPLATE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/aar.conf?rev=10074629#L64
 [MSVC\_FLAGS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L10069
 [MX\_FORMULAS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/mx_archive.py?rev=10074629#L1
 [NEED\_CHECK]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7184
 [NEED\_REVIEW]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7202
 [NGINX\_MODULES]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9960
 [NODE\_MODULES]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/ts.conf?rev=10074629#L76
 [NO\_BUILD\_IF]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [NO\_CHECK\_IMPORTS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7671
 [NO\_CLANG\_COVERAGE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7036
 [NO\_CLANG\_TIDY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7040
 [NO\_CODENAVIGATION]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6946
 [NO\_COMPILER\_WARNINGS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6908
 [NO\_CPU\_CHECK]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5776
 [NO\_CYTHON\_COVERAGE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7057
 [NO\_DEBUG\_INFO]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7506
 [NO\_DOCTESTS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2205
 [NO\_EXPORT\_DYNAMIC\_SYMBOLS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1857
 [NO\_EXTENDED\_SOURCE\_SEARCH]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1814
 [NO\_JOIN\_SRC]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7012
 [NO\_LIBC]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6976
 [NO\_LINT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2181
 [NO\_LTO]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L438
 [NO\_MYPY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L946
 [NO\_NEED\_CHECK]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7192
 [NO\_OPTIMIZE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6898
 [NO\_OPTIMIZE\_PY\_PROTOS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L668
 [NO\_PLATFORM]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6986
 [NO\_PLATFORM\_RESOURCES]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6938
 [NO\_PYTHON\_COVERAGE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7048
 [NO\_PYTHON\_INCLUDES]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5173
 [NO\_RUNTIME]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6965
 [NO\_SANITIZE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7020
 [NO\_SANITIZE\_COVERAGE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7028
 [NO\_SSE4]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5768
 [NO\_UTIL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6954
 [NO\_WERROR]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6924
 [NO\_WSHADOW]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6930
 [NVCC\_DEVICE\_LINK]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6885
 [ONLY\_TAGS]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [OPENSOURCE\_EXPORT\_REPLACEMENT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/opensource.conf?rev=10074629#L43
 [OPTIMIZE\_PY\_PROTOS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L658
 [ORIGINAL\_SOURCE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L10007
 [OWNER]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [PACK]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3127
 [PACKAGE\_STRICT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3132
 [PACK\_GLOBALS\_IN\_LIBRARY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2628
 [PARTITIONED\_RECURSE]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [PARTITIONED\_RECURSE\_FOR\_TESTS]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [PARTITIONED\_RECURSE\_ROOT\_RELATIVE]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [PEERDIR]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [PIRE\_INLINE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6701
 [PIRE\_INLINE\_CMD]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6696
 [PREPARE\_INDUCED\_DEPS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7311
 [PRIMARY\_OUTPUT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8232
 [PRINT\_MODULE\_TYPE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/print_module_type.py?rev=10074629#L1
 [PROCESS\_DOCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/docs.py?rev=10074629#L31
 [PROCESS\_MKDOCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/docs.py?rev=10074629#L43
 [PROGUARD\_RULES]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/aar.conf?rev=10074629#L13
 [PROTO2FBS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1012
 [PROTO\_ADDINCL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L630
 [PROTO\_NAMESPACE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L647
 [PROVIDES]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [PYTHON]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7387
 [PYTHON2\_ADDINCL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5189
 [PYTHON2\_MODULE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2878
 [PYTHON3\_ADDINCL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5236
 [PYTHON3\_MODULE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2890
 [PYTHON\_PATH]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2161
 [PY\_CONSTRUCTOR]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/pybuild.py?rev=10074629#L633
 [PY\_DOCTESTS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/pybuild.py?rev=10074629#L560
 [PY\_ENUMS\_SERIALIZATION]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/pybuild.py?rev=10074629#L648
 [PY\_EXTRA\_LINT\_FILES]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9582
 [PY\_MAIN]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/pybuild.py?rev=10074629#L616
 [PY\_NAMESPACE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3252
 [PY\_PROTOS\_FOR]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [PY\_PROTO\_PLUGIN]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L691
 [PY\_PROTO\_PLUGIN2]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L703
 [PY\_REGISTER]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/pybuild.py?rev=10074629#L578
 [PY\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9525
 [PY\_SSQLS\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9931
 [REAL\_LINK\_DYN\_LIB\_IMPL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1632
 [REAL\_LINK\_EXEC\_DYN\_LIB\_IMPL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1626
 [REAL\_LINK\_EXE\_IMPL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1620
 [RECURSE]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [RECURSE\_FOR\_TESTS]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [RECURSE\_ROOT\_RELATIVE]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [REGISTER\_SANDBOX\_IMPORT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/sandbox_registry.py?rev=10074629#L6
 [REGISTER\_YQL\_PYTHON\_UDF]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/yql_python_udf.py?rev=10074629#L10
 [REQUIREMENTS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2122
 [REQUIRES]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L516
 [RESOLVE\_PROTO]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3193
 [RESOURCE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L609
 [RESOURCE\_FILES]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/res.py?rev=10074629#L57
 [RESTRICT\_LICENSES]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/license.conf?rev=10074629#L401
 [RESTRICT\_PATH]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/macros_with_error.py?rev=10074629#L13
 [RUN]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/ytest.py?rev=10074629#L1040
 [RUN\_ANTLR]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7729
 [RUN\_ANTLR4]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7738
 [RUN\_ANTLR4\_CPP]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7750
 [RUN\_ANTLR4\_GO]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7758
 [RUN\_ANTLR4\_PYTHON]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7771
 [RUN\_JAVA\_PROGRAM]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3384
 [RUN\_LUA]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7362
 [RUN\_PROGRAM]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7336
 [RUN\_PYTHON3]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7413
 [SDBUS\_CPP\_ADAPTOR]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9901
 [SDBUS\_CPP\_PROXY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9907
 [SECONDARY\_OUTPUT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/aar.conf?rev=10074629#L338
 [SET]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [SETUP\_EXECTEST]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/ytest.py?rev=10074629#L1046
 [SETUP\_PYTEST\_BIN]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/ytest.py?rev=10074629#L1030
 [SETUP\_RUN\_PYTHON]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/ytest.py?rev=10074629#L1058
 [SET\_APPEND]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [SET\_APPEND\_WITH\_GLOBAL]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [SET\_COMPILE\_OUTPUTS\_MODIFIERS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5796
 [SET\_RESOURCE\_MAP\_FROM\_JSON]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [SET\_RESOURCE\_URI\_FROM\_JSON]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [SIZE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5638
 [SKIP\_TEST]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2170
 [SOURCE\_GROUP]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [SPLIT\_CODEGEN]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/split_codegen.py?rev=10074629#L9
 [SPLIT\_DWARF]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5426
 [SPLIT\_FACTOR]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5614
 [SRC]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6309
 [SRCDIR]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6328
 [SRC\_C\_AVX]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6439
 [SRC\_C\_AVX2]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6447
 [SRC\_C\_AVX512]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6455
 [SRC\_C\_NO\_LTO]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6537
 [SRC\_C\_PCLMUL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6472
 [SRC\_C\_PIC]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6529
 [SRC\_C\_SSE2]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6399
 [SRC\_C\_SSE3]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6407
 [SRC\_C\_SSE4]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6423
 [SRC\_C\_SSE41]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6431
 [SRC\_C\_SSSE3]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6415
 [SRC\_C\_XOP]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6464
 [SRC\_RESOURCE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3459
 [STRIP]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6892
 [STRUCT\_CODEGEN]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6820
 [STYLE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2314
 [STYLE\_PYTHON]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2197
 [SUBSCRIBER]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [SUPPRESSIONS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/suppressions.py?rev=10074629#L1
 [SYMLINK]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7253
 [SYSTEM\_PROPERTIES]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4489
 [TAG]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2111
 [TASKLET]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7792
 [TASKLET\_REG]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7809
 [TASKLET\_REG\_EXT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7824
 [TEST\_CWD]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4530
 [TEST\_DATA]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/ytest.py?rev=10074629#L41
 [TEST\_JAVA\_CLASSPATH\_CMD\_TYPE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5018
 [TEST\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2079
 [TIMEOUT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5559
 [TOUCH]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7657
 [TS\_TEST\_DATA]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/ts.conf?rev=10074629#L212
 [TS\_TEST\_FOR]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [TS\_TEST\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/ts.conf?rev=10074629#L191
 [UBERJAR]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4554
 [UBERJAR\_APPENDING\_TRANSFORMER]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4638
 [UBERJAR\_HIDE\_EXCLUDE\_PATTERN]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4582
 [UBERJAR\_HIDING\_PREFIX]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4567
 [UBERJAR\_MANIFEST\_TRANSFORMER\_ATTRIBUTE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4622
 [UBERJAR\_MANIFEST\_TRANSFORMER\_MAIN]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4609
 [UBERJAR\_PATH\_EXCLUDE\_PREFIX]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4596
 [UBERJAR\_SERVICES\_RESOURCE\_TRANSFORMER]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4651
 [UDF\_NO\_PROBE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/yql_udf.conf?rev=10074629#L28
 [UPDATE\_VCS\_JAVA\_INFO\_NODEP]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6752
 [USE\_COMMON\_GOOGLE\_APIS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L827
 [USE\_CXX]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6996
 [USE\_DYNAMIC\_CUDA]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1872
 [USE\_ERROR\_PRONE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4519
 [USE\_EXT\_PROTO]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8072
 [USE\_JAVALITE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L971
 [USE\_LINKER\_GOLD]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1455
 [USE\_MODERN\_FLEX]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/bison_lex.conf?rev=10074629#L84
 [USE\_MODERN\_FLEX\_WITH\_HEADER]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/bison_lex.conf?rev=10074629#L95
 [USE\_OLD\_FLEX]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/bison_lex.conf?rev=10074629#L104
 [USE\_PERL\_514\_LIB]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5329
 [USE\_PERL\_LIB]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5322
 [USE\_PLANTUML]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/docs.conf?rev=10074629#L311
 [USE\_PYTHON2]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5285
 [USE\_PYTHON3]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5302
 [USE\_RECIPE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2149
 [USE\_SKIFF]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L778
 [USE\_UTIL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7004
 [VALIDATE\_DATA\_RESTART]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5569
 [VERSION]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7210
 [VISIBILITY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9879
 [WERROR]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6917
 [WHOLE\_ARCHIVE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7785
 [WINDOWS\_MANIFEST]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9864
 [WITHOUT\_LICENSE\_TEXTS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L10028
 [WITH\_DYNAMIC\_LIBS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1614
 [WITH\_GROOVY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4857
 [WITH\_JDK]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4830
 [WITH\_KAPT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4848
 [WITH\_KOTLIN]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4839
 [WITH\_KOTLINC\_ALLOPEN]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4875
 [WITH\_KOTLINC\_LOMBOK]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4885
 [WITH\_KOTLINC\_NOARG]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4895
 [WITH\_KOTLINC\_SERIALIZATION]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L4905
 [XSTYPEMAPS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L280
 [XS\_PROTO]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1002
 [YABS\_GENERATE\_CONF]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/yabs_generate_conf.py?rev=10074629#L10
 [YABS\_GENERATE\_PHANTOM\_CONF\_PATCH]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/yabs_generate_conf.py?rev=10074629#L35
 [YABS\_GENERATE\_PHANTOM\_CONF\_TEST\_CHECK]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/yabs_generate_conf.py?rev=10074629#L53
 [YA\_CONF\_JSON]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L10101
 [YDL\_DESC\_USE\_BINARY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6300
 [YMAPS\_SPROTO]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/sproto.conf?rev=10074629#L16
 [YP\_PROTO\_YSON]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L891
 [YQL\_ABI\_VERSION]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/yql_udf.conf?rev=10074629#L127
 [YQL\_LAST\_ABI\_VERSION]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/yql_udf.conf?rev=10074629#L136
 [YT\_SPEC]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2068
 [\_AAR\_CMD\_IMPL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/aar.conf?rev=10074629#L305
 [\_ADD\_CLASSPATH\_CLASH\_CHECK]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/java.py?rev=10074629#L245
 [\_ADD\_CPP\_PROTO\_OUT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L725
 [\_ADD\_DYNLYB\_SEM]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2704
 [\_ADD\_EXTRA\_FLAGS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5812
 [\_ADD\_EXTRA\_FLAGS\_IMPL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5805
 [\_ADD\_GEN\_JAVA\_SCRIPT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3852
 [\_ADD\_HIDDEN\_INPUTS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3603
 [\_ADD\_JAVA\_STYLE\_CHECKS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/java.py?rev=10074629#L227
 [\_ADD\_KOTLIN\_STYLE\_CHECKS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/java.py?rev=10074629#L232
 [\_ADD\_OPTS\_IF\_NON\_EMPTY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3612
 [\_ADD\_PY\_PROTO\_OUT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L679
 [\_ADD\_SCU\_NAME]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6196
 [\_ADD\_YQL\_UDF\_DEPS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/yql_udf.conf?rev=10074629#L54
 [\_ALL\_PY\_SRCS2]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9535
 [\_APPEND\_DOCS\_DIR\_FLAG]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/docs.conf?rev=10074629#L329
 [\_ARCADIA\_PYTHON3\_ADDINCL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5246
 [\_ARCADIA\_PYTHON\_ADDINCL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5198
 [\_ARCHIVE\_SEM\_HELPER]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6681
 [\_ARF\_HELPER]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5531
 [\_BARE\_LINK\_MODULE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2567
 [\_BARE\_MODULE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2552
 [\_BUILDWITH\_CYTHON\_CPP\_DEP]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6557
 [\_BUILDWITH\_CYTHON\_CPP\_H]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6567
 [\_BUILDWITH\_CYTHON\_C\_API\_H]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6607
 [\_BUILDWITH\_CYTHON\_C\_DEP]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6588
 [\_BUILDWITH\_CYTHON\_C\_H]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6598
 [\_BUILD\_MNS\_CPP]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7141
 [\_BUILD\_MNS\_FILE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7135
 [\_BUILD\_MNS\_FILES]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/build_mn_files.py?rev=10074629#L4
 [\_BUILD\_MNS\_HEADER]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7145
 [\_BUNDLE\_TARGET]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5550
 [\_CHECK\_JAVA\_SRCDIR]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/java.py?rev=10074629#L267
 [\_CHECK\_RUN\_JAVA\_PROG\_CLASSPATH]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/java.py?rev=10074629#L322
 [\_COMPILE\_ASRC\_IMPL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/asrc.conf?rev=10074629#L42
 [\_CONDITIONAL\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2577
 [\_COPY\_FILES\_TO\_BUILD\_PREFIX]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/copy_files_to_build_prefix.py?rev=10074629#L10
 [\_COPY\_FILE\_IMPL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5497
 [\_CPP\_CFGPROTO\_CMD]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L930
 [\_CPP\_EVLOG\_CMD]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L917
 [\_CPP\_FLATC64\_CMD]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1125
 [\_CPP\_FLATC\_CMD]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1118
 [\_CPP\_PROTO\_CMD]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L904
 [\_CPP\_PROTO\_EVLOG\_CMD]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L923
 [\_CPP\_VANILLA\_PROTO\_CMD]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L911
 [\_DOCS\_LIBRARY\_CMD\_IMPL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/docs.conf?rev=10074629#L75
 [\_DOCS\_LIBRARY\_EPILOGUE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/docs.conf?rev=10074629#L106
 [\_DOCS\_MKDOCS\_CMD\_IMPL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/docs.conf?rev=10074629#L228
 [\_DOCS\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/docs.conf?rev=10074629#L98
 [\_DOCS\_YFM\_CMD\_IMPL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/docs.conf?rev=10074629#L44
 [\_DOCS\_YFM\_USE\_PLANTUML]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/docs.conf?rev=10074629#L128
 [\_DO\_1\_RUN\_JAR\_PROGRAM]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3379
 [\_DO\_2\_RUN\_JAR\_PROGRAM]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3371
 [\_EXPORT\_JAVA\_BINDINGS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/java.ymake.conf?rev=10074629#L163
 [\_EXPORT\_SWIG\_SOURCES]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/java.ymake.conf?rev=10074629#L167
 [\_FAT\_OBJECT\_ARGS\_BASE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L2624
 [\_FBS\_NAMESPACE\_IMPL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8111
 [\_FETCH\_CONTRIB]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3439
 [\_FILL\_JAR\_COPY\_RESOURCES\_CMD]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/java.py?rev=10074629#L290
 [\_FILL\_JAR\_GEN\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/java.py?rev=10074629#L302
 [\_FILTER\_EXTS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6171
 [\_FMT\_INDUCED\_DEPS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7286
 [\_FROM\_EXTERNAL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7463
 [\_FROM\_NPM\_LOCKFILES]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/nots.py?rev=10074629#L28
 [\_GENERATE\_PY\_EVS\_INTERNAL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5491
 [\_GENERATE\_PY\_PROTOS\_INTERNAL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5484
 [\_GENTAR\_HELPER]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3354
 [\_GEN\_JAVA\_SCRIPT\_IMPL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3846
 [\_GLOB]: https://a.yandex-team.ru/arc/trunk/arcadia/devtools/ymake/yndex/builtin.cpp?rev=10074629#L14
 [\_GO\_COMPILE\_CGO1]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8477
 [\_GO\_COMPILE\_CGO2]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8482
 [\_GO\_COMPILE\_SYMABIS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8471
 [\_GO\_EMBED\_DIR]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8653
 [\_GO\_EMBED\_PATTERN]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8614
 [\_GO\_FLATC\_CMD]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1137
 [\_GO\_GEN\_COVER\_GO]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8466
 [\_GO\_GRPC]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8719
 [\_GO\_GRPC\_GATEWAY\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8764
 [\_GO\_GRPC\_GATEWAY\_SRCS\_IMPL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8745
 [\_GO\_GRPC\_GATEWAY\_SWAGGER\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8770
 [\_GO\_LINK\_EXE\_IMPL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8496
 [\_GO\_LINK\_LIB\_IMPL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8491
 [\_GO\_LINK\_TEST\_IMPL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8501
 [\_GO\_PROCESS\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/gobuild.py?rev=10074629#L87
 [\_GO\_PROTO\_CMD]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L883
 [\_GO\_PROTO\_CMD\_IMPL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L876
 [\_GO\_RESOURCE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/gobuild.py?rev=10074629#L278
 [\_GO\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8530
 [\_GO\_UNUSED\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8558
 [\_HASH\_HELPER]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3349
 [\_INPUT\_WITH\_FLAG]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/java.ymake.conf?rev=10074629#L4
 [\_INPUT\_WITH\_FLAG\_IMPL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/java.ymake.conf?rev=10074629#L8
 [\_IOS\_ASSETS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9669
 [\_JAR\_ANN\_PROC\_OPTS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3400
 [\_JAR\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3330
 [\_JAVAC\_RUN\_HELPER]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3600
 [\_JAVA\_EVLOG\_CMD]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1038
 [\_JAVA\_FLATC\_CMD]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1149
 [\_JAVA\_PROTO\_CMD]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L992
 [\_JAVA\_PROTO\_PLUGIN\_ARGS\_BASE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L709
 [\_JDK\_VERSION\_MACRO\_CHECK]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/java.py?rev=10074629#L384
 [\_JNI\_CPP\_SWIG\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/java.ymake.conf?rev=10074629#L171
 [\_JNI\_JAVA\_SWIG\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/java.ymake.conf?rev=10074629#L176
 [\_JSRC\_PROXY\_MOBILE\_LIBRARY\_CMD\_IMPL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/asrc.conf?rev=10074629#L88
 [\_LANG\_CFLAGS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6176
 [\_LUAJIT\_21\_OBJDUMP]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7070
 [\_LUAJIT\_OBJDUMP]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7064
 [\_MAKE\_YQL\_PYTHON\_UDF\_TEST]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/yql_udf.conf?rev=10074629#L215
 [\_MAKE\_YQL\_UDF]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/yql_udf.conf?rev=10074629#L64
 [\_MAPKITIDL\_PROXY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/mapkit.conf?rev=10074629#L17
 [\_MARK\_JAVA\_PROG\_WITH\_SOURCES]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3888
 [\_MCU\_CONVERT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L10042
 [\_MKDOCS\_DOCS\_DIR]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/docs.conf?rev=10074629#L360
 [\_MKDOCS\_EPILOGUE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/docs.conf?rev=10074629#L253
 [\_MOBILE\_DLL\_PREREQUISITES\_CMD]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/asrc.conf?rev=10074629#L112
 [\_MOBILE\_LIBRARY\_PREREQUISITES\_CMD]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/asrc.conf?rev=10074629#L69
 [\_MOBILE\_LIBRARY\_PREREQUISITES\_IMPL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/asrc.conf?rev=10074629#L65
 [\_MOBILE\_TEST\_APK\_CMD\_IMPL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/aar.conf?rev=10074629#L114
 [\_MSVC\_FLAGS\_WINDOWS\_IMPL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L10060
 [\_MX\_BIN\_TO\_INFO]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7074
 [\_MX\_GEN\_TABLE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7086
 [\_NODE\_MODULES]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/ts.conf?rev=10074629#L80
 [\_NOOP\_MACRO]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3405
 [\_ORDER\_ADDINCL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L617
 [\_PACK\_JAR\_HELPER]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3595
 [\_PROTO\_DESC\_CMD]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7855
 [\_PROTO\_PLUGIN\_ARGS\_BASE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L673
 [\_PY3\_COMPILE\_BYTECODE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6677
 [\_PY3\_REGISTER]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6656
 [\_PYTHON3\_ADDINCL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5257
 [\_PYTHON\_ADDINCL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5207
 [\_PY\_COMPILE\_BYTECODE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6667
 [\_PY\_ENUM\_SERIALIZATION\_TO\_JSON]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9937
 [\_PY\_ENUM\_SERIALIZATION\_TO\_PY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9942
 [\_PY\_EVLOG\_CMD]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1028
 [\_PY\_EVLOG\_CMD\_BASE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1022
 [\_PY\_EVLOG\_CMD\_INTERNAL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1033
 [\_PY\_PROGRAM]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/pybuild.py?rev=10074629#L168
 [\_PY\_PROTO\_CMD]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L956
 [\_PY\_PROTO\_CMD\_BASE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L951
 [\_PY\_PROTO\_CMD\_INTERNAL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L961
 [\_PY\_REGISTER]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6645
 [\_PY\_SSQLS\_SRC]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9914
 [\_PY\_SSQLS\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9924
 [\_PY\_SSQLS\_SRC\_\_\_\_ssqls]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9919
 [\_PY\_TEST]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/ytest2.py?rev=10074629#L53
 [\_RAW\_PROTO\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8085
 [\_REGISTER\_NO\_CHECK\_IMPORTS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/ytest.py?rev=10074629#L662
 [\_REQUIRE\_EXPLICIT\_LICENSE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/license.conf?rev=10074629#L375
 [\_RESOURCE\_SEM]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L580
 [\_RUN\_JAVA]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7419
 [\_RUN\_JBUILD\_PROGRAM]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/java.py?rev=10074629#L34
 [\_SETUP\_GO\_GRPC\_GATEWAY]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L8758
 [\_SET\_DOCS\_BIN\_DIR\_FLAG]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/docs.conf?rev=10074629#L334
 [\_SET\_ENV\_FOR\_CUSTOM\_COMMAND]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7281
 [\_SET\_ENV\_FOR\_CUSTOM\_COMMAND\_IMPL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7274
 [\_SET\_FIRST\_VALUE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3240
 [\_SPLIT\_CODEGEN\_BASE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6806
 [\_SRC]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5825
 [\_SRCS\_NO\_GLOBAL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L3262
 [\_SRC\_CPP\_CUSTOM\_FLAGS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6340
 [\_SRC\_CUSTOM\_C\_CPP]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6351
 [\_SRC\_CUSTOM\_C\_CPP\_\_\_\_C]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6391
 [\_SRC\_CUSTOM\_C\_CPP\_\_\_\_c]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6359
 [\_SRC\_CUSTOM\_C\_CPP\_\_\_\_cc]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6383
 [\_SRC\_CUSTOM\_C\_CPP\_\_\_\_cpp]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6367
 [\_SRC\_CUSTOM\_C\_CPP\_\_\_\_cxx]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6375
 [\_SRC\_C\_CUSTOM\_FLAGS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6335
 [\_SRC\_STRICT\_C\_CPP]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6481
 [\_SRC\_STRICT\_C\_CPP\_\_\_\_C]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6521
 [\_SRC\_STRICT\_C\_CPP\_\_\_\_c]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6489
 [\_SRC\_STRICT\_C\_CPP\_\_\_\_cc]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6513
 [\_SRC\_STRICT\_C\_CPP\_\_\_\_cpp]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6497
 [\_SRC\_STRICT\_C\_CPP\_\_\_\_cxx]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6505
 [\_SRC\_\_\_\_C]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6051
 [\_SRC\_\_\_\_S]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5885
 [\_SRC\_\_\_\_asm]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6086
 [\_SRC\_\_\_\_asp]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5954
 [\_SRC\_\_\_\_c]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6056
 [\_SRC\_\_\_\_cc]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6045
 [\_SRC\_\_\_\_cfgproto]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5994
 [\_SRC\_\_\_\_cpp]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6034
 [\_SRC\_\_\_\_cu]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6106
 [\_SRC\_\_\_\_cxx]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6040
 [\_SRC\_\_\_\_ev]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5975
 [\_SRC\_\_\_\_f]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6027
 [\_SRC\_\_\_\_fbs]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6113
 [\_SRC\_\_\_\_fbs64]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6119
 [\_SRC\_\_\_\_fml]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5906
 [\_SRC\_\_\_\_fml2]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5911
 [\_SRC\_\_\_\_fml3]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5916
 [\_SRC\_\_\_\_gperf]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5935
 [\_SRC\_\_\_\_gztproto]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5986
 [\_SRC\_\_\_\_in]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6007
 [\_SRC\_\_\_\_l]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/bison_lex.conf?rev=10074629#L119
 [\_SRC\_\_\_\_lex]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/bison_lex.conf?rev=10074629#L126
 [\_SRC\_\_\_\_lpp]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/bison_lex.conf?rev=10074629#L131
 [\_SRC\_\_\_\_lua]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6092
 [\_SRC\_\_\_\_m]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6062
 [\_SRC\_\_\_\_masm]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6067
 [\_SRC\_\_\_\_mm]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5901
 [\_SRC\_\_\_\_pln]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5965
 [\_SRC\_\_\_\_po]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6257
 [\_SRC\_\_\_\_proto]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5980
 [\_SRC\_\_\_\_pysrc]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6124
 [\_SRC\_\_\_\_pyx]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5999
 [\_SRC\_\_\_\_rl]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5940
 [\_SRC\_\_\_\_rl5]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5949
 [\_SRC\_\_\_\_rl6]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5959
 [\_SRC\_\_\_\_rodata]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5879
 [\_SRC\_\_\_\_s]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5891
 [\_SRC\_\_\_\_s79]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5896
 [\_SRC\_\_\_\_sc]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6017
 [\_SRC\_\_\_\_sfdl]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5921
 [\_SRC\_\_\_\_ssqls]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6022
 [\_SRC\_\_\_\_storyboard]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9657
 [\_SRC\_\_\_\_swg]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5856
 [\_SRC\_\_\_\_xib]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L9662
 [\_SRC\_\_\_\_xs]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5930
 [\_SRC\_\_\_\_xsyn]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5944
 [\_SRC\_\_\_\_y]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/bison_lex.conf?rev=10074629#L109
 [\_SRC\_\_\_\_yasm]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6080
 [\_SRC\_\_\_\_ydl]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6266
 [\_SRC\_\_\_\_ypp]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/bison_lex.conf?rev=10074629#L114
 [\_SRC\_c]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6206
 [\_SRC\_c\_nodeps]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6149
 [\_SRC\_cpp]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6201
 [\_SRC\_lua\_21]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6233
 [\_SRC\_m]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6211
 [\_SRC\_masm]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6216
 [\_SRC\_py2src]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6131
 [\_SRC\_py3src]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6136
 [\_SRC\_yasm]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7715
 [\_SRC\_yasm\_helper]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7710
 [\_STYLE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/cpp_style.py?rev=10074629#L6
 [\_SWIG\_PYTHON\_C]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6626
 [\_SWIG\_PYTHON\_CPP]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L6617
 [\_TARGET\_SOURCES\_FOR\_HEADERS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7267
 [\_TARGET\_SOURCES\_FOR\_HEADERS\_IMPL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L7260
 [\_TS\_CONFIGURE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/nots.py?rev=10074629#L49
 [\_TS\_LIBRARY\_EPILOGUE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/ts.conf?rev=10074629#L222
 [\_TS\_TEST\_CONFIGURE]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/nots.py?rev=10074629#L75
 [\_UNITTEST]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/ytest2.py?rev=10074629#L42
 [\_USE\_LINKER]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1449
 [\_USE\_LINKER\_IMPL]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L1445
 [\_XS\_SRCS]: https://a.yandex-team.ru/arc/trunk/arcadia/build/ymake.core.conf?rev=10074629#L5925
 [\_YA\_CONF\_JSON]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/res.py?rev=10074629#L121
 [\_YFM\_DOCS\_DIR]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/docs.conf?rev=10074629#L342
 [\_YMAKE\_GENERATE\_SCRIPT]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/java.py?rev=10074629#L379
 [\_YMAPS\_GENERATE\_SPROTO\_HEADER]: https://a.yandex-team.ru/arc/trunk/arcadia/build/conf/project_specific/maps/sproto.conf?rev=10074629#L8
 [\_YTEST]: https://a.yandex-team.ru/arc/trunk/arcadia/build/plugins/ytest2.py?rev=10074629#L49
