# Copyright 2015 Google Inc. All rights reserved.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
cmake_minimum_required(VERSION 2.8.12)

project(flatuisample_3d)

add_executable(flatuisample_3d flatuisample_3d.cpp)
add_dependencies(flatuisample_3d fplbase flatui)
mathfu_configure_flags(flatuisample_3d)
target_link_libraries(flatuisample_3d fplbase flatui)

# FlatUI postprocess
flatui_post_process(flatuisample_3d "sample")
