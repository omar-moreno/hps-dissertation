#
# CMakeLists.txt
# @author Omar Moreno
# @date January 13, 2016
#

# Specify the minimum CMake version required.  If the cmake version 
# minimum is not met, cmake will fail.
cmake_minimum_required(VERSION 2.8 FATAL_ERROR)

# Set the name of the project
project(hps-thesis NONE)

# Include the file containing the CMake LaTeX macros required to build the
# document.
include(cmake/UseLATEX.cmake)

# Add the document to the build
add_latex_document(hps_thesis.tex
    INPUTS title_page.tex
           chapters/introduction.tex
           chapters/abstract.tex
           chapters/motivations.tex
           chapters/fixed_target.tex
           chapters/hps_apparatus.tex
           chapters/performance.tex
           chapters/event_selection.tex
           chapters/resonance.tex
           chapters/conclusion.tex
    BIBFILES chapters/bibliography.bib
    IMAGE_DIRS images
)
