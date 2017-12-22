*****************************************************************************************
 The NEON_2_SSE.h file is intended to simplify ARM->IA32 porting
 It makes the correspondence (or a real port) between ARM NEON intrinsics (as defined in "arm_neon.h") header
 and x86 SSE(up to SSE4.2) intrinsic functions as defined in corresponding x86 compilers headers files.
 ****************************************************************************************

To take advantage of this file just include it in your project that uses ARM NEON intinsics instead of "arm_neon.h", compile it as usual and enjoy the result.

For significant performance improvement in some cases you might need to define USE_SSE4 in your project settings. Otherwise SIMD up to SSSE3 to be used.

For more information and license please read the NEON_2_SSE.h content.
