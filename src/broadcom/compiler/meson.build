# Copyright © 2017 Broadcom
#
# Permission is hereby granted, free of charge, to any person obtaining a copy
# of this software and associated documentation files (the "Software"), to deal
# in the Software without restriction, including without limitation the rights
# to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
# copies of the Software, and to permit persons to whom the Software is
# furnished to do so, subject to the following conditions:
#
# The above copyright notice and this permission notice shall be included in
# all copies or substantial portions of the Software.
#
# THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
# IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
# FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
# AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
# LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
# OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
# SOFTWARE.

libbroadcom_compiler_files = files(
  'nir_to_vir.c',
  'vir.c',
  'vir_dump.c',
  'vir_live_variables.c',
  'vir_lower_uniforms.c',
  'vir_opt_copy_propagate.c',
  'vir_opt_dead_code.c',
  'vir_register_allocate.c',
  'vir_to_qpu.c',
  'qpu_schedule.c',
  'qpu_validate.c',
  'v3d_compiler.h',
  'v3d_nir_lower_io.c',
  'v3d_nir_lower_txf_ms.c',
)

libbroadcom_compiler = static_library(
  ['broadcom_compiler', v3d_xml_pack, nir_opcodes_h, nir_builder_opcodes_h],
  libbroadcom_compiler_files,
  include_directories : [inc_common, inc_broadcom],
  c_args : [c_vis_args, no_override_init_args],
  dependencies : [dep_libdrm, dep_valgrind],
  build_by_default : false,
)
