# Build script applied to the downloaded zip archive of the WPILib HAL library files for Athena.

# This file imports all the .so files inside the zip archive as individual cc_import targets,
# and then combines these targets into one cc_library target which can easily be consumed by higher level libs.

cc_import(
    name = "wpiHal",
    shared_library = "linux/athena/shared/libwpiHal.so",
)

#cc_import(
#    name = "wpiHalJni",
#    shared_library = "linux/athena/shared/libwpiHal.so",
#)

cc_library(
    name = "wpilib-hal-athena",
    visibility = ["@//third_party/wpilib:__pkg__"],
    deps = [
        ":wpiHal",
        #":wpiHalJni",
    ],
)
