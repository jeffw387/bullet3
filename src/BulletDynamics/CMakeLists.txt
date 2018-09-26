
add_library(BulletDynamics)
target_include_directories(BulletDynamics PUBLIC ${BULLET_PHYSICS_SOURCE_DIR}/src  )

SET(BulletDynamics_SRCS
	${CMAKE_CURRENT_SOURCE_DIR}/Character/btKinematicCharacterController.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btConeTwistConstraint.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btContactConstraint.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btFixedConstraint.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btGearConstraint.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btGeneric6DofConstraint.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btGeneric6DofSpringConstraint.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btGeneric6DofSpring2Constraint.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btHinge2Constraint.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btHingeConstraint.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btPoint2PointConstraint.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btSequentialImpulseConstraintSolver.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btSequentialImpulseConstraintSolverMt.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btBatchedConstraints.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btNNCGConstraintSolver.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btSliderConstraint.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btSolve2LinearConstraint.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btTypedConstraint.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btUniversalConstraint.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/Dynamics/btDiscreteDynamicsWorld.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/Dynamics/btDiscreteDynamicsWorldMt.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/Dynamics/btSimulationIslandManagerMt.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/Dynamics/btRigidBody.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/Dynamics/btSimpleDynamicsWorld.cpp
#	${CMAKE_CURRENT_SOURCE_DIR}/Dynamics/Bullet-C-API.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/Vehicle/btRaycastVehicle.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/Vehicle/btWheelInfo.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/Featherstone/btMultiBody.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/Featherstone/btMultiBodyConstraint.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/Featherstone/btMultiBodyConstraintSolver.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/Featherstone/btMultiBodyDynamicsWorld.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/Featherstone/btMultiBodyFixedConstraint.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/Featherstone/btMultiBodyGearConstraint.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/Featherstone/btMultiBodyJointLimitConstraint.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/Featherstone/btMultiBodyJointMotor.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/Featherstone/btMultiBodyMLCPConstraintSolver.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/Featherstone/btMultiBodyPoint2Point.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/Featherstone/btMultiBodySliderConstraint.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/MLCPSolvers/btDantzigLCP.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/MLCPSolvers/btMLCPSolver.cpp
	${CMAKE_CURRENT_SOURCE_DIR}/MLCPSolvers/btLemkeAlgorithm.cpp
)

SET(Root_HDRS
	${CMAKE_CURRENT_SOURCE_DIR}/../btBulletDynamicsCommon.h
	${CMAKE_CURRENT_SOURCE_DIR}/../btBulletCollisionCommon.h
)
SET(ConstraintSolver_HDRS
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btConeTwistConstraint.h
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btConstraintSolver.h
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btContactConstraint.h
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btContactSolverInfo.h
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btFixedConstraint.h
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btGearConstraint.h
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btGeneric6DofConstraint.h
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btGeneric6DofSpringConstraint.h
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btGeneric6DofSpring2Constraint.h
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btHinge2Constraint.h
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btHingeConstraint.h
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btJacobianEntry.h
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btPoint2PointConstraint.h
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btSequentialImpulseConstraintSolver.h
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btSequentialImpulseConstraintSolverMt.h
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btNNCGConstraintSolver.h
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btSliderConstraint.h
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btSolve2LinearConstraint.h
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btSolverBody.h
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btSolverConstraint.h
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btTypedConstraint.h
	${CMAKE_CURRENT_SOURCE_DIR}/ConstraintSolver/btUniversalConstraint.h
)
SET(Dynamics_HDRS
	${CMAKE_CURRENT_SOURCE_DIR}/Dynamics/btActionInterface.h
	${CMAKE_CURRENT_SOURCE_DIR}/Dynamics/btDiscreteDynamicsWorld.h
	${CMAKE_CURRENT_SOURCE_DIR}/Dynamics/btDiscreteDynamicsWorldMt.h
	${CMAKE_CURRENT_SOURCE_DIR}/Dynamics/btSimulationIslandManagerMt.h
	${CMAKE_CURRENT_SOURCE_DIR}/Dynamics/btDynamicsWorld.h
	${CMAKE_CURRENT_SOURCE_DIR}/Dynamics/btSimpleDynamicsWorld.h
	${CMAKE_CURRENT_SOURCE_DIR}/Dynamics/btRigidBody.h
)
SET(Vehicle_HDRS
	${CMAKE_CURRENT_SOURCE_DIR}/Vehicle/btRaycastVehicle.h
	${CMAKE_CURRENT_SOURCE_DIR}/Vehicle/btVehicleRaycaster.h
	${CMAKE_CURRENT_SOURCE_DIR}/Vehicle/btWheelInfo.h
)

SET(Featherstone_HDRS
	${CMAKE_CURRENT_SOURCE_DIR}/Featherstone/btMultiBody.h
	${CMAKE_CURRENT_SOURCE_DIR}/Featherstone/btMultiBodyConstraint.h
	${CMAKE_CURRENT_SOURCE_DIR}/Featherstone/btMultiBodyConstraintSolver.h
	${CMAKE_CURRENT_SOURCE_DIR}/Featherstone/btMultiBodyDynamicsWorld.h
	${CMAKE_CURRENT_SOURCE_DIR}/Featherstone/btMultiBodyFixedConstraint.h
	${CMAKE_CURRENT_SOURCE_DIR}/Featherstone/btMultiBodyGearConstraint.h
	${CMAKE_CURRENT_SOURCE_DIR}/Featherstone/btMultiBodyJointLimitConstraint.h
	${CMAKE_CURRENT_SOURCE_DIR}/Featherstone/btMultiBodyJointMotor.h
	${CMAKE_CURRENT_SOURCE_DIR}/Featherstone/btMultiBodyLink.h
	${CMAKE_CURRENT_SOURCE_DIR}/Featherstone/btMultiBodyLinkCollider.h
	${CMAKE_CURRENT_SOURCE_DIR}/Featherstone/btMultiBodyMLCPConstraintSolver.h
	${CMAKE_CURRENT_SOURCE_DIR}/Featherstone/btMultiBodyPoint2Point.h
	${CMAKE_CURRENT_SOURCE_DIR}/Featherstone/btMultiBodySliderConstraint.h
	${CMAKE_CURRENT_SOURCE_DIR}/Featherstone/btMultiBodySolverConstraint.h
)

SET(MLCPSolvers_HDRS
	${CMAKE_CURRENT_SOURCE_DIR}/MLCPSolvers/btDantzigLCP.h
	${CMAKE_CURRENT_SOURCE_DIR}/MLCPSolvers/btDantzigSolver.h
	${CMAKE_CURRENT_SOURCE_DIR}/MLCPSolvers/btMLCPSolver.h
	${CMAKE_CURRENT_SOURCE_DIR}/MLCPSolvers/btMLCPSolverInterface.h
	${CMAKE_CURRENT_SOURCE_DIR}/MLCPSolvers/btPATHSolver.h
	${CMAKE_CURRENT_SOURCE_DIR}/MLCPSolvers/btSolveProjectedGaussSeidel.h
	${CMAKE_CURRENT_SOURCE_DIR}/MLCPSolvers/btLemkeSolver.h
	${CMAKE_CURRENT_SOURCE_DIR}/MLCPSolvers/btLemkeAlgorithm.h
)

SET(Character_HDRS
	${CMAKE_CURRENT_SOURCE_DIR}/Character/btCharacterControllerInterface.h
	${CMAKE_CURRENT_SOURCE_DIR}/Character/btKinematicCharacterController.h
)



SET(BulletDynamics_HDRS
	${Root_HDRS}
	${ConstraintSolver_HDRS}
	${Dynamics_HDRS}
	${Vehicle_HDRS}
	${Character_HDRS}
	${Featherstone_HDRS}
	${MLCPSolvers_HDRS}
)


target_sources(BulletDynamics PRIVATE ${BulletDynamics_SRCS} PUBLIC ${BulletDynamics_HDRS})
SET_TARGET_PROPERTIES(BulletDynamics PROPERTIES VERSION ${BULLET_VERSION})
SET_TARGET_PROPERTIES(BulletDynamics PROPERTIES SOVERSION ${BULLET_VERSION})
IF (BUILD_SHARED_LIBS)
	TARGET_LINK_LIBRARIES(BulletDynamics BulletCollision LinearMath)
ENDIF (BUILD_SHARED_LIBS)

IF (INSTALL_LIBS)
	IF (NOT INTERNAL_CREATE_DISTRIBUTABLE_MSVC_PROJECTFILES)
		IF (${CMAKE_MAJOR_VERSION}.${CMAKE_MINOR_VERSION} GREATER 2.5)
			IF (APPLE AND BUILD_SHARED_LIBS AND FRAMEWORK)
				INSTALL(TARGETS BulletDynamics DESTINATION .)
			ELSE (APPLE AND BUILD_SHARED_LIBS AND FRAMEWORK)
				INSTALL(TARGETS BulletDynamics RUNTIME DESTINATION bin
								LIBRARY DESTINATION lib${LIB_SUFFIX}
								ARCHIVE DESTINATION lib${LIB_SUFFIX})
				INSTALL(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}
DESTINATION ${INCLUDE_INSTALL_DIR} FILES_MATCHING PATTERN "*.h"  PATTERN
".svn" EXCLUDE PATTERN "CMakeFiles" EXCLUDE)
				INSTALL(FILES ../btBulletDynamicsCommon.h
DESTINATION ${INCLUDE_INSTALL_DIR}/BulletDynamics)
			ENDIF (APPLE AND BUILD_SHARED_LIBS AND FRAMEWORK)
		ENDIF (${CMAKE_MAJOR_VERSION}.${CMAKE_MINOR_VERSION} GREATER 2.5)

		IF (APPLE AND BUILD_SHARED_LIBS AND FRAMEWORK)
			SET_TARGET_PROPERTIES(BulletDynamics PROPERTIES FRAMEWORK true)
			SET_TARGET_PROPERTIES(BulletDynamics PROPERTIES PUBLIC_HEADER "${Root_HDRS}")
			# Have to list out sub-directories manually:
			SET_PROPERTY(SOURCE ${ConstraintSolver_HDRS} PROPERTY MACOSX_PACKAGE_LOCATION Headers/ConstraintSolver)
			SET_PROPERTY(SOURCE ${Dynamics_HDRS} PROPERTY MACOSX_PACKAGE_LOCATION Headers/Dynamics)
			SET_PROPERTY(SOURCE ${Vehicle_HDRS} PROPERTY MACOSX_PACKAGE_LOCATION Headers/Vehicle)
			SET_PROPERTY(SOURCE ${Character_HDRS} PROPERTY MACOSX_PACKAGE_LOCATION Headers/Character)
			SET_PROPERTY(SOURCE ${Featherstone_HDRS} PROPERTY MACOSX_PACKAGE_LOCATION Headers/Featherstone)
			SET_PROPERTY(SOURCE ${MLCPSolvers_HDRS} PROPERTY MACOSX_PACKAGE_LOCATION Headers/MLCPSolvers)
		ENDIF (APPLE AND BUILD_SHARED_LIBS AND FRAMEWORK)
	ENDIF (NOT INTERNAL_CREATE_DISTRIBUTABLE_MSVC_PROJECTFILES)
ENDIF (INSTALL_LIBS)
