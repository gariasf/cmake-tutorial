add_library(MathFunctions
    MathFunctions.cxx
)


option(USE_MYMATH "Use tutorial provided math implementation" OFF)

if(USE_MYMATH)
    add_library(SqrtLibrary STATIC
        mysqrt.cxx
    )

    target_compile_definitions(MathFunctions PRIVATE SqrtLibrary)
endif()
