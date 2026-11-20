# AutoMLP - A workflow to generate deep potential force field
---------

AutoMLP is a code to:  
(1) Optimize neural network force field  
(2) Analyze CP2K and LAMMPS trajectory  

The code is mainly written in Python and Fortran.  

Email: lujunbo15@gmail.com
  
# Installation for AutoMLP

* Prerequisites
   - Python 3.5 or higher
   - Numpy 1.8.0 or higher

   Suggestion: as we will use deepmd-kit software, we recommend users could  
   install deepmd-kit at firsti: https://github.com/deepmodeling/deepmd-kit.   
   Then add the environmental variable of deepmd-kit, it will include python   
   and numpy.  

* Compile core module
  
    git clone https://github.com/JunboLu/AutoMLP.git  
    !Caution: When downloading AutoMLP through zip version, please change the  
    name "AutoMLP-main" to "AutoMLP" after you unzip it.  
    cd AutoMLP_directory/lib  
    change directory of f2py in Makefile  
    !Caution: If your gcc version is low, f2py cannot compile core code please  
    update your gcc up to 6.3.  
    make  

* Environmental variable

    !Caution: You may need to add environments of gcc  
    export PYTHONPATH=../AutoMLP_directory:$PYTHONPATH  
    change python_exe and AutoMLP directory in AutoMLP_directory/bin/AutoMLP file  
    export PATH=AutoMLP_directory/bin:$PATH  

# How to use 
* AutoMLP is an user-friendly code.  

  The input files are in example directory.  
  Users just need to run:  
  AutoMLP input.inp  
