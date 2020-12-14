# HPCA_Project_With_CUDA

Merge Sort Path and Batch Merge implementation with CUDA.
*Question 1.1 : Algo Merge Path of the Project
*Question 1.2 : Upgrade Algo
--> Representation of the merge path 1.2
--> Execution time algorithm 1.2
*Question 1.3 : Parallel MergeSort
*Question 2.4 : BATCH MERGE
*Question 2.5 : BATCH MERGE Execution time
*Application with Alice and Bob => Cryptography


Step 1- Files needed:  Makefile and functions.hpp available via Gists:
=> Makefile : https://gist.github.com/NajwaMoursli/f1b95b7d8ceb8d1abb8c446ece66960e/raw/Makefile \\
=> functions.hpp : https://gist.github.com/NajwaMoursli/5fe67ed5c22e84ba7a6331fcf4c79249 \\
The functions.hpp gist enables to create the src for compiling the project with the Makefile via the src/repos/functions repository on Google Collalb.

Step 2- The Google Collab Notebook (file .ipynb), uses GPU for execution, and nvidia-smi as the graphic card.

Step 3 => Install the Cudda Compiler : 
# Preparation
!nvcc --version
!pip install git+git://github.com/andreinechaev/nvcc4jupyter.git
!mkdir -p src/repos src/obj
%load_ext nvcc_plugin

Step 4 => Graphic Card for GPU use:
# Graphic Card Type. Better with Tesla T4 or higher T 
!nvidia-smi

Step 5 => Import the Gists needed and create the src repository 
!cd src  && rm -Rf Makefile && wget -P . https://gist.github.com/NajwaMoursli/f1b95b7d8ceb8d1abb8c446ece66960e/raw/Makefile

!rm -Rf src/repos/functions
!git clone https://gist.github.com/NajwaMoursli/5fe67ed5c22e84ba7a6331fcf4c79249 src/repos/functions

Step 6 => Now you can execute the codes with the command : 
%%cuda --name main.cu (on the top of the code cell, with the code you want to run)
!cd src && make
!cd src && make run 


Contributors: Najwa MOURSLI and Achille BAUCHER 
