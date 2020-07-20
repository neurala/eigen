# Eigen B4B SDK mirror

This repo mirrors the release of Eigen 3.3.7 retrieved from http://eigen.tuxfamily.org/index.php?title=News:Eigen_3.3.7_released!


## Changes over official release

* `EIGEN_HAS_CUDA_FP16` is unconditionally undefined to avoid name clashes between CUDA and OpenCL half types.
* `operator == (const half& a, const half& b)` and `operator != (const half& a, const half& b)` are commented out since they cause warnings with CUDA 11. We do not needed Eigen with FP16 at the moment.
* `abs(const std::complex<float>& x)` and `abs(const std::complex<double>& x)` are commented out, as CUDA 11 has issues with accessing the real and imaginary part of complex numbers.
