# ichello

This is a basic 'hello world' Python wrapped C++ application to demonstrate a sample packaging approach.

It uses `nanobind` to do the wrapping, defined in `src/binding.cpp`, `CMake` to build the module shared library, defined in `CMakeLists.txt` and `scikit-build-core` to interface the Python project definition in `pyproject.toml` and CMake.

To locally install and use the package you can do:

``` shell
pip install -e .
```

from the project directory.

Then you can do:

``` python
import ichello
ichello.get_sum([1.0, 2.0, 3.0])
>> 6.0
```

in a shell. The `get_sum` function is an instantiation of the template defined in `include.hpp` for the `double` type.



