package(
    default_testonly = 1,
    default_visibility = ["//src:__subpackages__"],
)

filegroup(
    name = "srcs",
    testonly = 0,
    srcs = glob(["**"]),
    visibility = ["//src/test/java/com/google/devtools/build/lib:__pkg__"],
)

java_library(
    name = "ObjcRulesTests_lib",
    srcs = [
        # TODO(b/64531582): Finish fixing all test files in this directory.
        "AppleBinaryTest.java",
        "AppleDynamicLibraryTest.java",
        "AppleStaticLibraryTest.java",
        "AppleStubBinaryTest.java",
        "AppleToolchainSelectionTest.java",
        "BinaryRuleType.java",
        "BinaryRuleTypePair.java",
        "HeaderDiscoveryTest.java",
        "HeaderThinningTest.java",
        "InterspersingTest.java",
        "IosDeviceTest.java",
        "J2ObjcLibraryTest.java",
        "J2ObjcSourceTest.java",
        "LegacyAppleBinaryTest.java",
        "LegacyAppleDynamicLibraryTest.java",
        "LegacyAppleStaticLibraryTest.java",
        "LegacyObjcBundleLibraryTest.java",
        "LegacyObjcBundleTest.java",
        "LegacyObjcFrameworkTest.java",
        "LegacyObjcImportTest.java",
        "LegacyObjcLibraryTest.java",
        "LegacyTest.java",
        "ObjcBundleLibraryTest.java",
        "ObjcBundleTest.java",
        "ObjcFrameworkTest.java",
        "ObjcImportTest.java",
        "ObjcLibraryTest.java",
        "ObjcProviderTest.java",
        "ObjcRuleTestCase.java",
        "ObjcSkylarkTest.java",
        "OnlyNeedsSourcesRuleType.java",
        "RuleType.java",
        "TargetDeviceFamilyTest.java",
        "ValueTest.java",
    ],
    deps = [
        "//src/main/java/com/google/devtools/build/lib:build-base",
        "//src/main/java/com/google/devtools/build/lib:packages-internal",
        "//src/main/java/com/google/devtools/build/lib:util",
        "//src/main/java/com/google/devtools/build/lib/actions",
        "//src/main/java/com/google/devtools/build/lib/cmdline",
        "//src/main/java/com/google/devtools/build/lib/collect/nestedset",
        "//src/main/java/com/google/devtools/build/lib/rules/apple",
        "//src/main/java/com/google/devtools/build/lib/rules/cpp",
        "//src/main/java/com/google/devtools/build/lib/rules/objc",
        "//src/main/java/com/google/devtools/build/lib/vfs",
        "//src/main/java/com/google/devtools/common/options",
        "//src/main/protobuf:bundlemerge_java_proto",
        "//src/main/protobuf:plmerge_java_proto",
        "//src/test/java/com/google/devtools/build/lib:actions_testutil",
        "//src/test/java/com/google/devtools/build/lib:analysis_testutil",
        "//src/test/java/com/google/devtools/build/lib:packages_testutil",
        "//src/test/java/com/google/devtools/build/lib:testutil",
        "//third_party:guava",
        "//third_party:guava-testlib",
        "//third_party:jsr305",
        "//third_party:junit4",
        "//third_party:truth",
        "//third_party/java/dd_plist",
    ],
)

java_test(
    name = "ObjcRulesTests",
    shard_count = 20,
    tags = ["no_windows"],
    test_class = "com.google.devtools.build.lib.AllTests",
    runtime_deps = [
        ":ObjcRulesTests_lib",
        "//src/main/java/com/google/devtools/build/lib:util",
        "//src/test/java/com/google/devtools/build/lib:testutil",
    ],
)

test_suite(
    name = "windows_tests",
    tags = [
        "-no_windows",
        "-slow",
    ],
    visibility = ["//visibility:private"],
)

test_suite(
    name = "all_windows_tests",
    tests = [
        ":windows_tests",
    ],
    visibility = ["//src/test/java/com/google/devtools/build/lib/rules:__pkg__"],
)
