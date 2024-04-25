set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${SCALAPACK_BINARY_DIR}/TESTING)

set (smatgen psmatgen.f pmatgeninc.f)
set (dmatgen pdmatgen.f pmatgeninc.f)
set (cmatgen pcmatgen.f pmatgeninc.f)
set (zmatgen pzmatgen.f pmatgeninc.f)

set (slinchk pslaschk.f pslafchk.f)
set (dlinchk pdlaschk.f pdlafchk.f)
set (clinchk pclaschk.f pclafchk.f)
set (zlinchk pzlaschk.f pzlafchk.f)

add_executable(xslu psludriver.f psluinfo.f psgetrrv.f ${smatgen} ${slinchk})
add_executable(xdlu pdludriver.f pdluinfo.f pdgetrrv.f ${dmatgen} ${dlinchk})
add_executable(xclu pcludriver.f pcluinfo.f pcgetrrv.f ${cmatgen} ${clinchk})
add_executable(xzlu pzludriver.f pzluinfo.f pzgetrrv.f ${zmatgen} ${zlinchk})

add_executable(xsdblu psdbdriver.f psdbinfo.f psdblaschk.f psdbmv1.f psbmatgen.f ${smatgen})
add_executable(xddblu pddbdriver.f pddbinfo.f pddblaschk.f pddbmv1.f pdbmatgen.f ${dmatgen})
add_executable(xcdblu pcdbdriver.f pcdbinfo.f pcdblaschk.f pcdbmv1.f pcbmatgen.f ${cmatgen})
add_executable(xzdblu pzdbdriver.f pzdbinfo.f pzdblaschk.f pzdbmv1.f pzbmatgen.f ${zmatgen})

add_executable(xsdtlu psdtdriver.f psdtinfo.f psdtlaschk.f psdbmv1.f psbmatgen.f ${smatgen})
add_executable(xddtlu pddtdriver.f pddtinfo.f pddtlaschk.f pddbmv1.f pdbmatgen.f ${dmatgen})
add_executable(xcdtlu pcdtdriver.f pcdtinfo.f pcdtlaschk.f pcdbmv1.f pcbmatgen.f ${cmatgen})
add_executable(xzdtlu pzdtdriver.f pzdtinfo.f pzdtlaschk.f pzdbmv1.f pzbmatgen.f ${zmatgen})

add_executable(xsgblu psgbdriver.f psgbinfo.f psdblaschk.f psgbmv1.f psbmatgen.f ${smatgen})
add_executable(xdgblu pdgbdriver.f pdgbinfo.f pddblaschk.f pdgbmv1.f pdbmatgen.f ${dmatgen})
add_executable(xcgblu pcgbdriver.f pcgbinfo.f pcdblaschk.f pcgbmv1.f pcbmatgen.f ${cmatgen})
add_executable(xzgblu pzgbdriver.f pzgbinfo.f pzdblaschk.f pzgbmv1.f pzbmatgen.f ${zmatgen})

add_executable(xsllt pslltdriver.f pslltinfo.f pspotrrv.f ${smatgen} ${slinchk})
add_executable(xdllt pdlltdriver.f pdlltinfo.f pdpotrrv.f ${dmatgen} ${dlinchk})
add_executable(xcllt pclltdriver.f pclltinfo.f pcpotrrv.f ${cmatgen} ${clinchk})
add_executable(xzllt pzlltdriver.f pzlltinfo.f pzpotrrv.f ${zmatgen} ${zlinchk})

add_executable(xspbllt pspbdriver.f pspbinfo.f pspblaschk.f pspbmv1.f psbmatgen.f ${smatgen})
add_executable(xdpbllt pdpbdriver.f pdpbinfo.f pdpblaschk.f pdpbmv1.f pdbmatgen.f ${dmatgen})
add_executable(xcpbllt pcpbdriver.f pcpbinfo.f pcpblaschk.f pcpbmv1.f pcbmatgen.f ${cmatgen})
add_executable(xzpbllt pzpbdriver.f pzpbinfo.f pzpblaschk.f pzpbmv1.f pzbmatgen.f ${zmatgen})

add_executable(xsptllt psptdriver.f psptinfo.f psptlaschk.f pspbmv1.f psbmatgen.f ${smatgen})
add_executable(xdptllt pdptdriver.f pdptinfo.f pdptlaschk.f pdpbmv1.f pdbmatgen.f ${dmatgen})
add_executable(xcptllt pcptdriver.f pcptinfo.f pcptlaschk.f pcpbmv1.f pcbmatgen.f ${cmatgen})
add_executable(xzptllt pzptdriver.f pzptinfo.f pzptlaschk.f pzpbmv1.f pzbmatgen.f ${zmatgen})

add_executable(xsinv psinvdriver.f psinvinfo.f psinvchk.f ${smatgen})
add_executable(xdinv pdinvdriver.f pdinvinfo.f pdinvchk.f ${dmatgen})
add_executable(xcinv pcinvdriver.f pcinvinfo.f pcinvchk.f ${cmatgen})
add_executable(xzinv pzinvdriver.f pzinvinfo.f pzinvchk.f ${zmatgen})

add_executable(xsqr psqrdriver.f psqrinfo.f psgeqrrv.f psgeqlrv.f psgelqrv.f psgerqrv.f pstzrzrv.f pslafchk.f ${smatgen})
add_executable(xdqr pdqrdriver.f pdqrinfo.f pdgeqrrv.f pdgeqlrv.f pdgelqrv.f pdgerqrv.f pdtzrzrv.f pdlafchk.f ${dmatgen})
add_executable(xcqr pcqrdriver.f pcqrinfo.f pcgeqrrv.f pcgeqlrv.f pcgelqrv.f pcgerqrv.f pctzrzrv.f pclafchk.f ${cmatgen})
add_executable(xzqr pzqrdriver.f pzqrinfo.f pzgeqrrv.f pzgeqlrv.f pzgelqrv.f pzgerqrv.f pztzrzrv.f pzlafchk.f ${zmatgen})

add_executable(xsls pslsdriver.f pslsinfo.f psqrt13.f psqrt14.f psqrt16.f psqrt17.f ${smatgen})
add_executable(xdls pdlsdriver.f pdlsinfo.f pdqrt13.f pdqrt14.f pdqrt16.f pdqrt17.f ${dmatgen})
add_executable(xcls pclsdriver.f pclsinfo.f pcqrt13.f pcqrt14.f pcqrt16.f pcqrt17.f ${cmatgen})
add_executable(xzls pzlsdriver.f pzlsinfo.f pzqrt13.f pzqrt14.f pzqrt16.f pzqrt17.f ${zmatgen})


target_link_libraries(xslu SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)
target_link_libraries(xdlu SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)
target_link_libraries(xclu SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)
target_link_libraries(xzlu SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)

target_link_libraries(xsdblu SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)
target_link_libraries(xddblu SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)
target_link_libraries(xcdblu SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)
target_link_libraries(xzdblu SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)

target_link_libraries(xsdtlu SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)
target_link_libraries(xddtlu SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)
target_link_libraries(xcdtlu SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)
target_link_libraries(xzdtlu SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)

target_link_libraries(xsgblu SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)
target_link_libraries(xdgblu SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)
target_link_libraries(xcgblu SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)
target_link_libraries(xzgblu SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)

target_link_libraries(xsllt SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)
target_link_libraries(xdllt SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)
target_link_libraries(xcllt SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)
target_link_libraries(xzllt SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)

target_link_libraries(xspbllt SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)
target_link_libraries(xdpbllt SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)
target_link_libraries(xcpbllt SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)
target_link_libraries(xzpbllt SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)

target_link_libraries(xsptllt SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)
target_link_libraries(xdptllt SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)
target_link_libraries(xcptllt SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)
target_link_libraries(xzptllt SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)

target_link_libraries(xsinv SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)
target_link_libraries(xdinv SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)
target_link_libraries(xcinv SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)
target_link_libraries(xzinv SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)

target_link_libraries(xsqr SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)
target_link_libraries(xdqr SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)
target_link_libraries(xcqr SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)
target_link_libraries(xzqr SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)

target_link_libraries(xsls SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)
target_link_libraries(xdls SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)
target_link_libraries(xcls SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)
target_link_libraries(xzls SCALAPACK::SCALAPACK ${LAPACK_LIBRARIES} ${BLAS_LIBRARIES} MPI::MPI_Fortran)

if ("${CMAKE_Fortran_COMPILER_ID}" STREQUAL "GNU" AND CMAKE_Fortran_COMPILER_VERSION VERSION_GREATER_EQUAL 10)
    set( CMAKE_Fortran_FLAGS "${CMAKE_Fortran_FLAGS} -std=legacy" )  # local to this directory
endif()
