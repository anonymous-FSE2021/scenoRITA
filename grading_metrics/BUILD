load("@rules_python//python:defs.bzl", "py_binary")

package(default_visibility = ["//visibility:public"])

py_binary(
	name = "collision",
	srcs = ["collision.py"],
	deps = [
		"//automation/auxiliary/record:read_record",
		"//modules/tools/perception:replay_perception"
	],
)

py_binary(
	name = "acceleration",
	srcs = ["acceleration.py"],
	deps = [
		"//automation/auxiliary/record:read_record",
		"//automation/grading_metrics:speeding",
	],
)

py_binary(
	name = "speeding",
	srcs = ["speeding.py"],
	deps = [
		"//automation/auxiliary/record:read_record",
		"//automation/auxiliary/map:map_tools",
		"//automation/grading_metrics:collision",
	],
)

py_binary(
	name = "off_road",
	srcs = ["off_road.py"],
	deps = [
		"//automation/auxiliary/record:read_record",
		"//automation/auxiliary/map:map_tools",
	],
)

py_binary(
	name = "run_oracles",
	srcs = ["run_oracles.py"],
	deps = [
		"//automation/grading_metrics:acceleration",
		"//automation/grading_metrics:collision",
		"//automation/grading_metrics:off_road",
		"//automation/grading_metrics:speeding",
	],
)
