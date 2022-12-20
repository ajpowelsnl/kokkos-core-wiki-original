# Deprecation

<!--- VERSION 3 DEPRECATION --->

## Kokkos-3.x

  |  **Deprecated**  |  **Replacement**  |  **Reason**
  |  ------------  | ------------  |  ------------
  |  `is_reducer_type` |  `is_reducer`  |  Improve API
  |  Array reductions with raw pointer  |  Use `View` as return argument  |  Improve API
  |  `OffsetView` constructors taking `index_list_type`  |  `pair` (CPU and GPU)  |  Streamline arguments to `::pair` function
  |  Overloads of `sort` taking a parameter `bool always_use_kokkos_sort`  |  Use `BinSort` if required, or call `sort` without bool parameter  |  Updating overloads
  |  |  **PUBLIC HEADERS UPDATES**
  |  Guard against non-public header inclusion  |  **Core PUBLIC HEADERS**:  |  Improve API
  |  | `Kokkos_Core.hpp`,
  |  | `Kokkos_Macros.hpp`,
  |  | `Kokkos_Atomic.hpp`,
  |  | `Kokkos_DetectionIdiom.hpp`,
  |  | `Kokkos_MathematicalConstants.hpp`,
  |  | `Kokkos_MathematicalFunctions.hpp`,
  |  | `Kokkos_NumericTraits.hpp`,
  |  | `Kokkos_Array.hpp`,
  |  | `Kokkos_Complex.hpp`,
  |  | `Kokkos_Pair.hpp`,
  |  | `Kokkos_Half.hpp`,
  |  | `Kokkos_Timer.hpp`
  |  Guard against non-public header inclusion  |  **Algorithms PUBLIC HEADERS**:  |  Improve API
  |  |  `Kokkos_StdAlgorithms.hpp`
  |  |  `Kokkos_Random.hpp`,
  |  |  `Kokkos_Sort.hpp`
  |  Guard against non-public header inclusion  |  **Containers PUBLIC HEADERS**:  | Improve API
  |  |  `Kokkos_Bitset.hpp`,
  |  |  `Kokkos_DualView.hpp`,
  |  |  `Kokkos_DynRankView.hpp`,
  |  |  `Kokkos_ErrorReporter.hpp`,
  |  |  `Kokkos_Functional.hpp`,
  |  |  `Kokkos_OffsetView.hpp`,
  |  |  `Kokkos_ScatterView.hpp`,
  |  |  `Kokkos_StaticCrsGraph.hpp`,
  |  |  `Kokkos_UnorderedMap.hpp`,
  |  |  `Kokkos_Vector.hpp`
  |  `Kokkos_UniqueToken.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_Threads.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_Serial.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_AnonymousSpace.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_Atomics_Desul_Config.hpp` not a public header  |  `Kokkos_Atomic.hpp`  |  Improve API
  |  `Kokkos_Vectorization.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_OpenACC.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_OpenACCSpace.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_MasterLock.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_View.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_ExecPolicy.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_Future.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_GraphNode.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_HBWSpace.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_ScratchSpace.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_Crs.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_SYCL_Space.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_SYCL.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_Cuda.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_CudaSpace.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `KokkosExp_MDRangePolicy.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_Tuners.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_HIP_Space.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_HIP.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_Rank.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_Atomics_Desul_Volatile_Wrapper.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_Atomics_Desul_Wrapper.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_MinMaxClamp.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_Concepts.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_MemoryPool.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_Parallel_Reduce.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_TaskScheduler.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_TaskScheduler_fwd.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_hwloc.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_PointerOwnership.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_OpenMPTarget.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_OpenMPTargetSpace.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_Layout.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_MemoryTraits.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_LogicalSpaces.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_Extents.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  `Kokkos_WorkGraph.hpp` not a public header  |  `Kokkos_Core.hpp`  |  Improve API
  |  Raise deprecation warnings if non-empty WorkTag class is used  |  Use empty WorkTag class  |  Improve API
  |  `std::string ProfilingSection::getName()`  |  Remove function  |  Improve API
  |  `uint32_t ProfilingSection::getSectionID()`  |  Remove function           |  Improve API
  |  `const std::string ProfilingSection::secName;`  |  Remove variable  |  Improve API
  |  `ActiveExecutionMemorySpace`  |  Remove type alias  |  Improve API
  |  `Impl::is_array_layout`  |  Remove type alias  |  Improve API
  |  `Impl::is_execution_policy`  |  Remove type alias  |  Improve API
  |  `Impl::is_execution_space`  |  Remove type alias  |  Improve API
  |  `Impl::is_memory_space`  |  Remove type alias  |  Improve API
  |  `Impl::is_memory_traits`  |  Remove type alias  |  Improve API
  |  `is_space::host_memory_space`  |  Remove type alias  |  Improve API
  |  `is_space::host_execution_space`  |  Remove type alias  |  Improve API
  |  `is_space::host_mirror_space`  |  Remove type alias  |  Improve API
  |  `Impl::is_space`  |  Remove type alias  |  Improve API
  |  `Impl::SpaceAccessibility`  |  Remove type alias  |  Improve API
  |  `KOKKOS_RESTRICT_EXECUTION_TO_DATA(DATA_SPACE, DATA_PTR)`  |  Remove macro  |  Improve API
  |  `KOKKOS_RESTRICT_EXECUTION_TO_(DATA_SPACE)`  |  Remove macro  |  Improve API
  |  `parallel_*` overloads taking the label as trailing argument  |  `parallel_*("KokkosViewLabel", policy, f);`  |  Consistent ordering of parameters
  |  Embedded types (`argument_type`, `first_argument_type`, and `second_argument_type`) in `std::function`  |  Use `decltype` (if required)  |  Align with deprecation in `std::function`
  |  `InitArguments` struct | `InitializationSettings()` class object with query-able attributes  |  Verifiable initialization
  |  `finalize_all()`  |  `finalize()`  |  Improve  API
  |  |  **COMMAND LINE ARGUMENTS UPDATES**
  |  Command-line arguments (other than `--help`) not prefixed with `kokkos-*`  | **UPDATED COMMAND-LINE ARGUMENTS**:  |  Improve API
  |  |  `--kokkos-num-threads`,
  |  |  `--kokkos-device-id`,
  |  |  `--kokkos-num-devices`
  |  `--[kokkos-]numa` command-line argument and `KOKKOS_NUMA` environment variable  |  `--kokkos-num-threads`  |  Align option nomenclature with `std::thread`
  |  `--[kokkos-]threads` command-line argument  |  `--kokkos-num-threads`  |  Improve API
  |  Warn about `parallel_reduce` cases that call `join()` with arguments qualified by `volatile` keyword  |  Remove `volatile` overloads  |  Streamline API
  |  `static void partition_master(F const& f, int requested_num_partitions = 0, int requested_partition_size = 0)`  |  Remove function  |  Improve API
  |  `void OpenMPInternal::validate_partition_impl(const int nthreads, int &num_partitions, int &partition_size)`  |  Remove function  |  Improve API
  |  `std::vector<OpenMP> OpenMP::partition(...)`  |  Remove function  |  Improve API
  |  `OpenMP OpenMP::create_instance(...)`  |  Remove function  |  Improve API
  |  `static void validate_partition(const int nthreads, int& num_partitions, int& partition_size)`  |  Remove function  |  Improve API
  |  `!std::is_void<T>::value &&`  |  `std::is_empty<T>::value &&` (C++17)  |  Improve API
  |  `static void validate_partition_impl(const int nthreads, int& num_partitions, int& partition_size)`  |  Remove function  |  Improve API
  |  `void OpenMP::partition_master(F const& f, int num_partitions, int partition_size)`  |  Remove function  |  Improve API
  |  `class MasterLock<OpenMP>`  |  Remove class  |  Improve API
  |  `class KOKKOS_ATTRIBUTE_NODISCARD ScopeGuard`  |  Remove class  |  Improve API
  |  `create_mirror_view` taking `WithOutInitializing` as first argument | `create_mirror_view(Impl::WithoutInitializing_t wi, View<T, P...> const& v)`  |  Improve API
  |  `!std::is_empty<typename base_t::work_tag>::value && !std::is_void<typename base_t::work_tag>::value`  |  Remove condition  |  Improve API
  |  `partition(...)`, `partition_master` for HPX backend  |  Remove function  |  Improve API
  |  `constexpr`  |  Remove specifier  |  Improve API
  |  `KOKKOS_THREAD_LOCAL` macro  |  `thread_local`  |  Improve API
  |  `vector_length() const`  |  Remove function  |  Improve API
  |  `class MasterLock`  |  Remove class  |  Improve API
  |  `Impl::is_view`  |  `is_view`  |  Improve API
  |  `inline int vector_length() const`  |  Remove function  |  Improve API
  |  |  **CUDA DEPRECATION**
  |  `void CudaSpace::access_error()`  |  Remove function  |  Improve API
  |  `int CudaUVMSpace::number_of_allocations()` |  Remove function  |  Improve API
  |  `inline void cuda_internal_safe_call_deprecated()`  |  `KOKKOS_IMPL CUDA_SAFE_CALL(call)`  |  Improve API
  |  `static void access_error();`  |  Remove function  |  Improve API
  |  `static void access_error(const void* const);`  |  Remove function
  |  `static int number_of_allocations();`  |  Remove function  |  Improve API
  |  |  **HIP DEPRECATION**
  |  `void Experimental::HIPSpace::access_error()`  |  Remove function  |  Improve API
  |  `void Experimental::HIPSpace::access_error(const void* const)`  |  Remove function  |  Improve API
  |  `int vector_length() const`  |  Remove function
  |  `inline void hip_internal_safe_call_deprecated  |  Remove function  |  Improve API
  |  `HIP_SAFE_CALL(call)`  |  Remove macro  |  Improve API
  |  |**SYCL DEPRECATION**
  |  |  **PROMOTION TO KOKKOKS NAMESPACE**
  |  `Experimental::aMathFunction`  |  Use `namespace Kokkos`  |  Promote to Kokkos namespace
  |  `Experimental::clamp`  |  Use `namespace Kokkos`  |  Promote to Kokkos namespace
  |  `Experimental::max;`  |  Use `namespace Kokkos`  |  Promote to Kokkos namespace
  |  `Experimental::min;`  |  Use `namespace Kokkos`  |  Promote to Kokkos namespace
  |  `Experimental::minmax;`  |  Use `namespace Kokkos`  |  Promote to Kokkos namespace
  |  `Experimental::Iterate`  |  Remove type alias  |  Improve API
  |  `Experiemntal::MDRangePolicy`  |  Remove type alias  |  Improve API
  |  `Experiemntal::Rank`  |  Remove type alias  |  Improve API
