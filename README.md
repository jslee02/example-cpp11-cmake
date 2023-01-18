# [Codecov][1] CI CMake g++ cpp11 lcov Example

[![CMake](https://github.com/jslee02/example-cpp11-cmake/actions/workflows/cmake.yml/badge.svg)](https://github.com/jslee02/example-cpp11-cmake/actions/workflows/cmake.yml)
[![codecov][codecov-badge]][codecov-link]

The goal of this project is to build project with following tools:
 * C++ version: `C++11`
 * Build system: [`CMake`](https://cmake.org/)
 * C++ compiler: `g++` or Visual Studio
 * Libraries: `STL` only
 * Code coverage report: [`lcov`](http://ltp.sourceforge.net/coverage/lcov.php) and [`OpenCppCoverage`](https://github.com/OpenCppCoverage/OpenCppCoverage)(note: it should show the code coverage is below 100%)
 * [`CodeCov`](https://codecov.io/) (code coverage is measured by CodeCov).
 * Source: multiple files

## Prerequisites
To build the project you need to install `CMake`. ([Install instructions](https://cmake.org/install/))
To display a code coverage report in the console, install `lcov`. ([`Download lcov`](http://ltp.sourceforge.net/coverage/lcov.php), [`Instructions`](http://ltp.sourceforge.net/coverage/lcov/readme.php))

## Guide
1. Compile with code coverage instrumentation enabled [(GCC)](https://gcc.gnu.org/onlinedocs/gcc/Instrumentation-Options.html).
2. Execute the tests to generate the coverage data.
3. (Optionally) generate and customize reports with `lcov`.
4. Upload to CodeCov using the bash uploader.

## Example details
This repo can serve as the starting point for a new project. The following is worth noticing:
1. Use of a build script instead of putting the commands into `.travis.yml`
  - Allows local testing
  - Allows usage of `set -e` to error out with meaningfull messages on any command failure
2. Separate testing source tree
  - Allows to easily enable/disable testing
  - Allows usage in parent projects (you don't want to build the tests if you are consumed)
  - You may want to exclude coverage of test files which is easier when they are in a separate folder.
    Remember to use **full paths** for patterns (like `'*/tests/*'`)

## Authors
* **RokKos** - [RokKos](https://github.com/RokKos)
* **Rolf Eike Beer** - [DerDakon](https://github.com/DerDakon)
* **Alexander Grund** - [Flamefire](https://github.com/Flamefire)

## License
This project is licensed under the MIT License - see the [LICENSE](https://github.com/RokKos/classes-c-/blob/master/LICENSE) file for details.

1. More documentation at https://docs.codecov.io
2. Configure codecov through the `codecov.yml` https://docs.codecov.io/docs/codecov-yaml

We are happy to help if you have any questions. Please email our Support at [support@codecov.io](mailto:support@codecov.io)

[1]: https://codecov.io/
[license-badge]:   https://img.shields.io/badge/license-MIT-007EC7.svg
[codecov-link]:    https://codecov.io/gh/jslee02/example-cpp11-cmake
[codecov-image]:   https://github.com/jslee02/example-cpp1-cmake/blob/master/img/Codecov.png
