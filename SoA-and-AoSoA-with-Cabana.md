# Structure of Arrays and Structure of Arrays with Cabana

[Cabana](https://github.com/ECP-copa/Cabana) is a MPI+Kokkos performance portable library for particle-based simulations.  It provides particle data structures, algorithms, and utilities to enable simulations on a variety of platforms including many-core architectures and GPUs.

This use case describes the SoA and AoSoA classes provided by Cabana.  Their goal is to provide a vectorization-friendly collections of contiguous elements that exhibit good alignment.

## Structure of Arrays (SoA)

### `Cabana::SoA`
Defined in header [`<Cabana_SoA.hpp>`](https://github.com/ECP-copa/Cabana/blob/master/core/src/Cabana_SoA.hpp)
```C++
template <typename DataTypes, int VectorLength>
struct SoA;
```

`Cabana::SoA` is a struct template that provides a way to store a fixed-size collection of heterogeneous arrays whose size is the specified vector length.

Conceptually `Cabana::SoA<Cabana::MemberTypes<float[3], char>, 8>` is equivalent to `std::tuple<float[3][8], char[8]>`.

The data structure keeps a separate, homogeneous data array for each particle field, each having the same number of elements.  The motivation is easier vectorization for the compiler.


#### Template parameters
`DataTypes`
: The types of the elements that the SoA stores as fixed size arrays.
It is required to be a specialization of `Cabana::MemberTypes` which is defined as
```C++
template <typename... Types>
MemberTypes<Types...>;
```

`VectorLength`
: The number of elements stored in contiguous memory locations for each data type.

#### Non-member functions
`Cabana::get`
: accesses the specified element of the SoA.