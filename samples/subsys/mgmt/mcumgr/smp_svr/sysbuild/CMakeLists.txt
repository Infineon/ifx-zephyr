# SPDX-License-Identifier: Apache-2.0

if(NOT DEFINED mcuboot_EXTRA_CONF_FILE AND BOARD MATCHES "^cy8cproto_062s3_4343w(/|$)")
  set(mcuboot_EXTRA_CONF_FILE ${CMAKE_CURRENT_LIST_DIR}/mcuboot_cy8cproto_062s3_4343w.conf
      CACHE INTERNAL "MCUboot sector layout for 512 B write-block flash")
endif()

find_package(Sysbuild REQUIRED HINTS $ENV{ZEPHYR_BASE})

project(sysbuild LANGUAGES)
