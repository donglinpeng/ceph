# unittest_mds_authcap
add_executable(unittest_mds_authcap
  TestMDSAuthCaps.cc
  $<TARGET_OBJECTS:unit-main>
  )
add_ceph_unittest(unittest_mds_authcap ${CMAKE_RUNTIME_OUTPUT_DIRECTORY}/unittest_mds_authcap)
target_link_libraries(unittest_mds_authcap mds global ${BLKID_LIBRARIES})

# unittest_mds_sessionfilter
add_executable(unittest_mds_sessionfilter
  TestSessionFilter.cc
  $<TARGET_OBJECTS:common_util_obj>
  $<TARGET_OBJECTS:unit-main>
  )
add_ceph_unittest(unittest_mds_sessionfilter ${CMAKE_RUNTIME_OUTPUT_DIRECTORY}/unittest_mds_sessionfilter)
target_link_libraries(unittest_mds_sessionfilter mds osdc common global ${BLKID_LIBRARIES})

