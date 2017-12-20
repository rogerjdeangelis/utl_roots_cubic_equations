# utl_roots_cubic_equations
Using SAS/WPS and Python for roots of a cubic equation

    ```  SAS-L: Finding the cube roots of x**3 + 8, there are three of them using Python  ```
    ```    ```
    ```     WORKING CODE  (Two solutions)  ```
    ```     Pyhton seems a little ahead of R for these types of solutions  ```
    ```    ```
    ```     1. Using SYMPY  ```
    ```    ```
    ```          x=symbols("x");  ```
    ```          y=solve (x**3+8,x);  ```
    ```          print(Y);  ```
    ```    ```
    ```        [-2,1+sqrt(3)i,1-sqrt(3)i]  ```
    ```    ```
    ```     2. Using NUMPY  ```
    ```    ```
    ```        /* x**3 + (0*x**2 + 0*x) + 8 = 0 */  ```
    ```        p = [1,0,0,8];  ```
    ```        roots=np.roots(p);  ```
    ```    ```
    ```        [-2+0.j,1.+1.73205081j, 1.-1.73205081j]  ```
    ```    ```
    ```    ```
    ```     3.  USING DE_MOIVRE FORMULA  ```
    ```    ```
    ```        see the Wiki link below (using De_Moivre Formula)  ```
    ```    ```
    ```        def cuberoot( z ):;  ```
    ```        .    z = complex(z);  ```
    ```        .    x = z.real;  ```
    ```        .    y = z.imag;  ```
    ```        .    mag = abs(z);  ```
    ```        .    arg = math.atan2(y,x);  ```
    ```        .    resMag = mag**(1./3);  ```
    ```        .    resArg = [ (arg+2*math.pi*n)/3. for n in range(1,4) ];  ```
    ```        .    return [  resMag*(math.cos(a) + math.sin(a)*1j) for a in resArg ];  ```
    ```    ```
    ```        [-2+4e-16j  1+1.73205081j    1-1.73205081j]  ```
    ```    ```
    ```    ```
    ```  De Moivre's formula can be derived from Eulers formula.  ```
    ```  We saw a little of this with my 'Fun with constants relationships  ```
    ```    ```
    ```  also see  ```
    ```  https://math.vanderbilt.edu/schectex/courses/cubic/  ```
    ```    ```
    ```  see  ```
    ```  https://en.wikipedia.org/wiki/De_Moivre%27s_formula  ```
    ```    ```
    ```  also see  ```
    ```  https://goo.gl/fQcp2w  ```
    ```  https://stackoverflow.com/questions/1361740/cubic-root-of-the-negative-number-on-python/1362288  ```
    ```    ```
    ```  Andrew Walker Profile  ```
    ```  https://stackoverflow.com/users/2246/andrew-walker  ```
    ```    ```
    ```  Daniel profile  ```
    ```  https://stackoverflow.com/users/3295073/daniel  ```
    ```    ```
    ```    ```
    ```  HAVE  ```
    ```  ====  ```
    ```    ```
    ```    Solve for the three roots  ```
    ```    ```
    ```     x**3 + 8 = 0  ```
    ```    ```
    ```    ```
    ```    ```
    ```  WANT  ```
    ```  ====  ```
    ```    ```
    ```   SYMPY      [-2,         1+sqrt(3)i,      1-sqrt(3)i]  ```
    ```    ```
    ```   NUMPY      [-2.+0j     1+1.73205081j    1-1.73205081j]  ```
    ```    ```
    ```   De Moivre  [-2+4e-16j  1+1.73205081j    1-1.73205081j]  ```
    ```    ```
    ```     sustituting into x**3 + 8 = -8 + 8 =0  ```
    ```    ```
    ```  *                _              _       _  ```
    ```   _ __ ___   __ _| | _____    __| | __ _| |_ __ _  ```
    ```  | '_ ` _ \ / _` | |/ / _ \  / _` |/ _` | __/ _` |  ```
    ```  | | | | | | (_| |   <  __/ | (_| | (_| | || (_| |  ```
    ```  |_| |_| |_|\__,_|_|\_\___|  \__,_|\__,_|\__\__,_|  ```
    ```    ```
    ```  ;  ```
    ```    ```
    ```    Just supply  ```
    ```    ```
    ```       x**3 + 8 = 0  ```
    ```    ```
    ```  *  ```
    ```   ___ _   _ _ __ ___  _ __  _   _  ```
    ```  / __| | | | '_ ` _ \| '_ \| | | |  ```
    ```  \__ \ |_| | | | | | | |_) | |_| |  ```
    ```  |___/\__, |_| |_| |_| .__/ \__, |  ```
    ```       |___/          |_|    |___/  ```
    ```  ;  ```
    ```    ```
    ```  %utl_submit_py64('  ```
    ```  from sympy import Symbol, solve;  ```
    ```  x = Symbol("x");  ```
    ```  y=solve(x**3 + 8);  ```
    ```  print(y);  ```
    ```  ');  ```
    ```  *  ```
    ```   _ __  _   _ _ __ ___  _ __  _   _  ```
    ```  | '_ \| | | | '_ ` _ \| '_ \| | | |  ```
    ```  | | | | |_| | | | | | | |_) | |_| |  ```
    ```  |_| |_|\__,_|_| |_| |_| .__/ \__, |  ```
    ```                        |_|    |___/  ```
    ```  ;  ```
    ```    ```
    ```  /* x**3 + (0*x**2 + 0*x) + 8 = 0 */  ```
    ```  %utl_submit_py64('  ```
    ```  import numpy as np;  ```
    ```  p = [1,0,0,8];  ```
    ```  roots=np.roots(p);  ```
    ```  print(roots);  ```
    ```  ');  ```
    ```    ```
    ```    ```
    ```  *____         __  __       _  ```
    ```  |  _ \  ___  |  \/  | ___ (_)_   ___ __ ___  ```
    ```  | | | |/ _ \ | |\/| |/ _ \| \ \ / / '__/ _ \  ```
    ```  | |_| |  __/ | |  | | (_) | |\ V /| | |  __/  ```
    ```  |____/ \___| |_|  |_|\___/|_| \_/ |_|  \___|  ```
    ```    ```
    ```  ;  ```
    ```    ```
    ```  %utl_submit_py64('  ```
    ```  import math;  ```
    ```  def cuberoot( z ):;  ```
    ```  .    z = complex(z);  ```
    ```  .    x = z.real;  ```
    ```  .    y = z.imag;  ```
    ```  .    mag = abs(z);  ```
    ```  .    arg = math.atan2(y,x);  ```
    ```  .    resMag = mag**(1./3);  ```
    ```  .    resArg = [ (arg+2*math.pi*n)/3. for n in range(1,4) ];  ```
    ```  .    return [  -1 * resMag*(math.cos(a) + math.sin(a)*1j) for a in resArg ];  ```
    ```  roots=cuberoot(8);  ```
    ```  print(roots);  ```
    ```  ');  ```
    ```    ```
