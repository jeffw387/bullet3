add_library(BulletCollision)
target_include_directories(BulletCollision PUBLIC ${BULLET_PHYSICS_SOURCE_DIR}/src)

SET(BulletCollision_SRCS
	${CMAKE_CURRENT_SOURCE_DIR}/BroadphaseCollision/btAxisSweep3.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/BroadphaseCollision/btBroadphaseProxy.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/BroadphaseCollision/btCollisionAlgorithm.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/BroadphaseCollision/btDbvt.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/BroadphaseCollision/btDbvtBroadphase.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/BroadphaseCollision/btDispatcher.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/BroadphaseCollision/btOverlappingPairCache.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/BroadphaseCollision/btQuantizedBvh.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/BroadphaseCollision/btSimpleBroadphase.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btActivatingCollisionAlgorithm.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btBoxBoxCollisionAlgorithm.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btBox2dBox2dCollisionAlgorithm.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btBoxBoxDetector.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btCollisionDispatcher.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btCollisionDispatcherMt.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btCollisionObject.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btCollisionWorld.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btCollisionWorldImporter.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btCompoundCollisionAlgorithm.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btCompoundCompoundCollisionAlgorithm.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btConvexConcaveCollisionAlgorithm.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btConvexConvexAlgorithm.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btConvexPlaneCollisionAlgorithm.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btConvex2dConvex2dAlgorithm.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btDefaultCollisionConfiguration.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btEmptyCollisionAlgorithm.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btGhostObject.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btHashedSimplePairCache.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btInternalEdgeUtility.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btInternalEdgeUtility.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btManifoldResult.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btSimulationIslandManager.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btSphereBoxCollisionAlgorithm.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btSphereSphereCollisionAlgorithm.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btSphereTriangleCollisionAlgorithm.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btUnionFind.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/SphereTriangleDetector.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btBoxShape.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btBox2dShape.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btBvhTriangleMeshShape.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btCapsuleShape.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btCollisionShape.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btCompoundShape.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btConcaveShape.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btConeShape.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btConvexHullShape.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btConvexInternalShape.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btConvexPointCloudShape.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btConvexPolyhedron.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btConvexShape.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btConvex2dShape.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btConvexTriangleMeshShape.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btCylinderShape.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btEmptyShape.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btHeightfieldTerrainShape.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btMiniSDF.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btMinkowskiSumShape.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btMultimaterialTriangleMeshShape.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btMultiSphereShape.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btOptimizedBvh.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btPolyhedralConvexShape.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btScaledBvhTriangleMeshShape.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btSdfCollisionShape.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btShapeHull.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btSphereShape.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btStaticPlaneShape.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btStridingMeshInterface.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btTetrahedronShape.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btTriangleBuffer.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btTriangleCallback.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btTriangleIndexVertexArray.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btTriangleIndexVertexMaterialArray.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btTriangleMesh.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btTriangleMeshShape.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btUniformScalingShape.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/btContactProcessing.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/btGenericPoolAllocator.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/btGImpactBvh.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/btGImpactCollisionAlgorithm.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/btGImpactQuantizedBvh.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/btGImpactShape.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/btTriangleShapeEx.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/gim_box_set.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/gim_contact.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/gim_memory.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/gim_tri_collision.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/NarrowPhaseCollision/btContinuousConvexCollision.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/NarrowPhaseCollision/btConvexCast.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/NarrowPhaseCollision/btGjkConvexCast.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/NarrowPhaseCollision/btGjkEpa2.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/NarrowPhaseCollision/btGjkEpaPenetrationDepthSolver.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/NarrowPhaseCollision/btGjkPairDetector.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/NarrowPhaseCollision/btMinkowskiPenetrationDepthSolver.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/NarrowPhaseCollision/btPersistentManifold.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/NarrowPhaseCollision/btRaycastCallback.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/NarrowPhaseCollision/btSubSimplexConvexCast.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/NarrowPhaseCollision/btVoronoiSimplexSolver.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/NarrowPhaseCollision/btPolyhedralContactClipping.cpp
)

SET(Root_HDRS
	${CMAKE_CURRENT_SOURCE_DIR}/../btBulletCollisionCommon.h
)
SET(BroadphaseCollision_HDRS
  ${CMAKE_CURRENT_SOURCE_DIR}/BroadphaseCollision/btAxisSweep3Internal.h
	${CMAKE_CURRENT_SOURCE_DIR}/BroadphaseCollision/btAxisSweep3.h
	${CMAKE_CURRENT_SOURCE_DIR}/BroadphaseCollision/btBroadphaseInterface.h
	${CMAKE_CURRENT_SOURCE_DIR}/BroadphaseCollision/btBroadphaseProxy.h
	${CMAKE_CURRENT_SOURCE_DIR}/BroadphaseCollision/btCollisionAlgorithm.h
	${CMAKE_CURRENT_SOURCE_DIR}/BroadphaseCollision/btDbvt.h
	${CMAKE_CURRENT_SOURCE_DIR}/BroadphaseCollision/btDbvtBroadphase.h
	${CMAKE_CURRENT_SOURCE_DIR}/BroadphaseCollision/btDispatcher.h
	${CMAKE_CURRENT_SOURCE_DIR}/BroadphaseCollision/btOverlappingPairCache.h
	${CMAKE_CURRENT_SOURCE_DIR}/BroadphaseCollision/btOverlappingPairCallback.h
	${CMAKE_CURRENT_SOURCE_DIR}/BroadphaseCollision/btQuantizedBvh.h
	${CMAKE_CURRENT_SOURCE_DIR}/BroadphaseCollision/btSimpleBroadphase.h
)
SET(CollisionDispatch_HDRS
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btActivatingCollisionAlgorithm.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btBoxBoxCollisionAlgorithm.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btBox2dBox2dCollisionAlgorithm.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btBoxBoxDetector.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btCollisionConfiguration.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btCollisionCreateFunc.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btCollisionDispatcher.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btCollisionDispatcherMt.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btCollisionObject.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btCollisionObjectWrapper.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btCollisionWorld.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btCollisionWorldImporter.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btCompoundCollisionAlgorithm.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btCompoundCompoundCollisionAlgorithm.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btConvexConcaveCollisionAlgorithm.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btConvexConvexAlgorithm.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btConvex2dConvex2dAlgorithm.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btConvexPlaneCollisionAlgorithm.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btDefaultCollisionConfiguration.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btEmptyCollisionAlgorithm.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btGhostObject.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btHashedSimplePairCache.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btManifoldResult.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btSimulationIslandManager.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btSphereBoxCollisionAlgorithm.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btSphereSphereCollisionAlgorithm.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btSphereTriangleCollisionAlgorithm.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/btUnionFind.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionDispatch/SphereTriangleDetector.h
)
SET(CollisionShapes_HDRS
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btBoxShape.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btBox2dShape.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btBvhTriangleMeshShape.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btCapsuleShape.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btCollisionMargin.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btCollisionShape.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btCompoundShape.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btConcaveShape.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btConeShape.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btConvexHullShape.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btConvexInternalShape.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btConvexPointCloudShape.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btConvexPolyhedron.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btConvexShape.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btConvex2dShape.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btConvexTriangleMeshShape.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btCylinderShape.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btEmptyShape.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btHeightfieldTerrainShape.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btMaterial.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btMinkowskiSumShape.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btMultimaterialTriangleMeshShape.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btMultiSphereShape.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btOptimizedBvh.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btPolyhedralConvexShape.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btScaledBvhTriangleMeshShape.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btShapeHull.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btSphereShape.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btStaticPlaneShape.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btStridingMeshInterface.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btTetrahedronShape.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btTriangleBuffer.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btTriangleCallback.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btTriangleIndexVertexArray.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btTriangleIndexVertexMaterialArray.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btTriangleInfoMap.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btTriangleMesh.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btTriangleMeshShape.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btTriangleShape.h
	${CMAKE_CURRENT_SOURCE_DIR}/CollisionShapes/btUniformScalingShape.h
)
SET(Gimpact_HDRS
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/btBoxCollision.h
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/btClipPolygon.h
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/btContactProcessingStructs.h
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/btContactProcessing.h
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/btGenericPoolAllocator.h
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/btGeometryOperations.h
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/btGImpactBvhStructs.h
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/btGImpactBvh.h
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/btGImpactCollisionAlgorithm.h
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/btGImpactMassUtil.h
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/btGImpactQuantizedBvhStructs.h
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/btGImpactQuantizedBvh.h
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/btGImpactShape.h
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/btQuantization.h
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/btTriangleShapeEx.h
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/gim_array.h
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/gim_basic_geometry_operations.h
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/gim_bitset.h
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/gim_box_collision.h
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/gim_box_set.h
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/gim_clip_polygon.h
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/gim_contact.h
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/gim_geom_types.h
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/gim_geometry.h
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/gim_hash_table.h
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/gim_linear_math.h
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/gim_math.h
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/gim_memory.h
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/gim_radixsort.h
	${CMAKE_CURRENT_SOURCE_DIR}/Gimpact/gim_tri_collision.h
)
SET(NarrowPhaseCollision_HDRS
	${CMAKE_CURRENT_SOURCE_DIR}/NarrowPhaseCollision/btContinuousConvexCollision.h
	${CMAKE_CURRENT_SOURCE_DIR}/NarrowPhaseCollision/btConvexCast.h
	${CMAKE_CURRENT_SOURCE_DIR}/NarrowPhaseCollision/btConvexPenetrationDepthSolver.h
	${CMAKE_CURRENT_SOURCE_DIR}/NarrowPhaseCollision/btDiscreteCollisionDetectorInterface.h
	${CMAKE_CURRENT_SOURCE_DIR}/NarrowPhaseCollision/btGjkConvexCast.h
	${CMAKE_CURRENT_SOURCE_DIR}/NarrowPhaseCollision/btGjkEpa2.h
	${CMAKE_CURRENT_SOURCE_DIR}/NarrowPhaseCollision/btGjkEpaPenetrationDepthSolver.h
	${CMAKE_CURRENT_SOURCE_DIR}/NarrowPhaseCollision/btGjkPairDetector.h
	${CMAKE_CURRENT_SOURCE_DIR}/NarrowPhaseCollision/btManifoldPoint.h
	${CMAKE_CURRENT_SOURCE_DIR}/NarrowPhaseCollision/btMinkowskiPenetrationDepthSolver.h
	${CMAKE_CURRENT_SOURCE_DIR}/NarrowPhaseCollision/btPersistentManifold.h
	${CMAKE_CURRENT_SOURCE_DIR}/NarrowPhaseCollision/btPointCollector.h
	${CMAKE_CURRENT_SOURCE_DIR}/NarrowPhaseCollision/btRaycastCallback.h
	${CMAKE_CURRENT_SOURCE_DIR}/NarrowPhaseCollision/btSimplexSolverInterface.h
	${CMAKE_CURRENT_SOURCE_DIR}/NarrowPhaseCollision/btSubSimplexConvexCast.h
	${CMAKE_CURRENT_SOURCE_DIR}/NarrowPhaseCollision/btVoronoiSimplexSolver.h
	${CMAKE_CURRENT_SOURCE_DIR}/NarrowPhaseCollision/btPolyhedralContactClipping.h
)

SET(BulletCollision_HDRS
	${Root_HDRS}
	${BroadphaseCollision_HDRS}
	${CollisionDispatch_HDRS}
	${CollisionShapes_HDRS}
	${Gimpact_HDRS}
	${NarrowPhaseCollision_HDRS}
)


target_sources(BulletCollision PRIVATE ${BulletCollision_SRCS} PUBLIC ${BulletCollision_HDRS})
SET_TARGET_PROPERTIES(BulletCollision PROPERTIES VERSION ${BULLET_VERSION})
SET_TARGET_PROPERTIES(BulletCollision PROPERTIES SOVERSION ${BULLET_VERSION})
IF (BUILD_SHARED_LIBS)
  TARGET_LINK_LIBRARIES(BulletCollision LinearMath)
ENDIF (BUILD_SHARED_LIBS)


IF (INSTALL_LIBS)
	IF (NOT INTERNAL_CREATE_DISTRIBUTABLE_MSVC_PROJECTFILES)
		#INSTALL of other files requires CMake 2.6
		IF (${CMAKE_MAJOR_VERSION}.${CMAKE_MINOR_VERSION} GREATER 2.5)
			IF (APPLE AND BUILD_SHARED_LIBS AND FRAMEWORK)
				INSTALL(TARGETS BulletCollision DESTINATION .)
			ELSE (APPLE AND BUILD_SHARED_LIBS AND FRAMEWORK)
				INSTALL(TARGETS BulletCollision RUNTIME DESTINATION bin
								LIBRARY DESTINATION lib${LIB_SUFFIX}
								ARCHIVE DESTINATION lib${LIB_SUFFIX})
				INSTALL(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}
DESTINATION ${INCLUDE_INSTALL_DIR} FILES_MATCHING PATTERN "*.h" PATTERN ".svn" EXCLUDE PATTERN "CMakeFiles" EXCLUDE)
				INSTALL(FILES ../btBulletCollisionCommon.h
DESTINATION ${INCLUDE_INSTALL_DIR}/BulletCollision)
			ENDIF (APPLE AND BUILD_SHARED_LIBS AND FRAMEWORK)
		ENDIF (${CMAKE_MAJOR_VERSION}.${CMAKE_MINOR_VERSION} GREATER 2.5)

		IF (APPLE AND BUILD_SHARED_LIBS AND FRAMEWORK)
			SET_TARGET_PROPERTIES(BulletCollision PROPERTIES FRAMEWORK true)

			SET_TARGET_PROPERTIES(BulletCollision PROPERTIES PUBLIC_HEADER "${Root_HDRS}")
			# Have to list out sub-directories manually:
			SET_PROPERTY(SOURCE ${BroadphaseCollision_HDRS} PROPERTY MACOSX_PACKAGE_LOCATION Headers/BroadphaseCollision)
			SET_PROPERTY(SOURCE ${CollisionDispatch_HDRS} PROPERTY MACOSX_PACKAGE_LOCATION Headers/CollisionDispatch)
			SET_PROPERTY(SOURCE ${CollisionShapes_HDRS} PROPERTY MACOSX_PACKAGE_LOCATION Headers/CollisionShapes)
			SET_PROPERTY(SOURCE ${Gimpact_HDRS} PROPERTY MACOSX_PACKAGE_LOCATION Headers/Gimpact)
			SET_PROPERTY(SOURCE ${NarrowPhaseCollision_HDRS} PROPERTY MACOSX_PACKAGE_LOCATION Headers/NarrowPhaseCollision)

		ENDIF (APPLE AND BUILD_SHARED_LIBS AND FRAMEWORK)
	ENDIF (NOT INTERNAL_CREATE_DISTRIBUTABLE_MSVC_PROJECTFILES)
ENDIF (INSTALL_LIBS)
