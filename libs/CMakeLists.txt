add_library(stella-parser
    antlr/stellaLexer.cpp
    antlr/stellaParser.cpp
    antlr/stellaParserBaseVisitor.cpp
    antlr/stellaParserVisitor.cpp
)

target_link_libraries(stella-parser PUBLIC antlr4_static)

target_include_directories(
    stella-parser
    SYSTEM
    INTERFACE
    $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/antlr>
)