itk_module_test()

set(ITKIOSTLMeshTests
  itkSTLMeshIOTest.cxx
)

CreateTestDriver(ITKIOSTLMesh "${ITKIOSTLMesh-Test_LIBRARIES}" "${ITKIOSTLMeshTests}" )

itk_add_test(NAME itkSTLMeshIOTest00
      COMMAND ITKIOSTLMeshTestDriver itkSTLMeshIOTest
      DATA{Baseline/sphere.vtk}
      ${ITK_TEST_OUTPUT_DIR}/sphere00.stl
      0  # write in ASCII
)

itk_add_test(NAME itkSTLMeshIOTest01
      COMMAND ITKIOSTLMeshTestDriver itkSTLMeshIOTest
      DATA{Baseline/sphere.vtk}
      ${ITK_TEST_OUTPUT_DIR}/sphere01.stl
      1  # write in BINARY
)

itk_add_test(NAME itkSTLMeshIOTest02
      COMMAND ITKIOSTLMeshTestDriver itkSTLMeshIOTest
      DATA{Baseline/sphere.stl}
      ${ITK_TEST_OUTPUT_DIR}/sphere02.stl
      0  # write in ASCII
)

itk_add_test(NAME itkSTLMeshIOTest03
      COMMAND ITKIOSTLMeshTestDriver itkSTLMeshIOTest
      DATA{Baseline/sphere.stl}
      ${ITK_TEST_OUTPUT_DIR}/sphere03.stl
      1  # write in BINARY
)

itk_add_test(NAME itkSTLMeshIOTest04
      COMMAND ITKIOSTLMeshTestDriver itkSTLMeshIOTest
      DATA{Baseline/tetrahedron.vtk}
      ${ITK_TEST_OUTPUT_DIR}/tetrahedron01.stl
      0  # write in ASCII
)

itk_add_test(NAME itkSTLMeshIOTest05
      COMMAND ITKIOSTLMeshTestDriver itkSTLMeshIOTest
      DATA{Baseline/tetrahedron.vtk}
      ${ITK_TEST_OUTPUT_DIR}/tetrahedron02.stl
      1  # write in BINARY
)

itk_add_test(NAME itkSTLMeshIOTest06
      COMMAND ITKIOSTLMeshTestDriver itkSTLMeshIOTest
      DATA{Baseline/tetrahedron.stl}
      ${ITK_TEST_OUTPUT_DIR}/tetrahedron03.stl
      0  # write in ASCII
)

itk_add_test(NAME itkSTLMeshIOTest07
      COMMAND ITKIOSTLMeshTestDriver itkSTLMeshIOTest
      DATA{Baseline/tetrahedron.stl}
      ${ITK_TEST_OUTPUT_DIR}/tetrahedron04.stl
      1  # write in BINARY
)
