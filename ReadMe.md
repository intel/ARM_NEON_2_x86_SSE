*****************************************************************************************
 The NEON_2_SSE.h file is intended to simplify ARM->IA32 porting.
 It makes the correspondence (or a real porting) of ARM NEON intrinsics as defined in "arm_neon.h" header
 and x86 SIMD (up to AVX2) intrinsic functions as defined in corresponding x86 compilers headers files.
 ****************************************************************************************

To take advantage of this file just include it in your project that uses ARM NEON intinsics instead of "arm_neon.h", compile it as usual and enjoy the result.

Considering 64-128 bit width of the NEON istructions AVX vector instructions usage in x86 implementaion is litited, SSE is used in more than 90% of functions.
However for some functions significant performance improvement it is recommended to compile your x86 code  with the highest level of vector instructions supported by the target CPU -say  SSE4 or AVX2.
Please notice that AVX2 enabling for this project compilation includes FMA instructions as well.
Just use the corresponding compiler flags for the purpose. In some cases you might need to define USE_SSE4 or USE_AVX2 in your project settings manually. Otherwise by default SIMD up to SSSE3 to be used.

If NEON2SSE_DISABLE_PERFORMANCE_WARNING macro is defined, then the performance warnings for serial functions implementaions are disabled. 

For more information and license please read the NEON_2_SSE.h content.

The unit tests set used for ARM NEON - x86 SSE conformance verification is  https://github.com/christophe-lyon/arm-neon-tests
