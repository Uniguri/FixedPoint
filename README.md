# FixedPoint
Single header file for fixed point for C++17.

# Usage
```C++
#include <iostream>

#include "fixed_point.hpp"

using namespace fixed_point;

int main() {
  // FixedPoint == FixedPoint<16>
  constexpr FixedPoint<16> fp0{1.1};  // This will be compile time constant.
  constexpr FixedPoint<16> fp1{1.1};  // This will be compile time constant.
  std::cout << fp0 << ' ' << fp1 << std::endl;
  constexpr double d0 =
      static_cast<double>(fp0);  // This will be compile time constant.
  constexpr double d1 =
      static_cast<double>(fp1);  // This will be compile time constant.
  std::cout << d0 << ' ' << d1 << std::endl;
  std::cout << fp0 + fp1 << std::endl;
  std::cout << fp0 - fp1 << std::endl;
  std::cout << fp0 * fp1 << std::endl;
  std::cout << fp0 / fp1 << std::endl;

  std::cout << "==========" << std::endl;

  FixedPoint<16> fp2;
  std::cin >> fp2;
  std::cout << fp2 << std::endl;
  std::cout << FixedPoint<>::floor(fp2) << std::endl;
  std::cout << FixedPoint<>::ceil(fp2) << std::endl;
  std::cout << FixedPoint<>::round(fp2) << std::endl;
  std::cout << FixedPoint<>::abs(fp2) << std::endl;
  std::cout << FixedPoint<>::sin(fp2) << std::endl;
  std::cout << FixedPoint<>::cos(fp2) << std::endl;
  std::cout << FixedPoint<>::tan(fp2) << std::endl;
  std::cout << FixedPoint<>::exp(fp2) << std::endl;
  std::cout << FixedPoint<>::log(fp2) << std::endl;
}
```

# Reference
- http://www.sunshine2k.de/articles/coding/fp/sunfp.html