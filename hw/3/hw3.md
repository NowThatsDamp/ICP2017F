1.)
```Bash
function [result] = untitled2(x,mu,sigma)
Half1 = (1/((sqrt(2*pi))*sigma));
Half2 = exp((-.5)*(((x-mu)/sigma)^2));
result = Half1*Half2;
end

>> untitled2(1,0,2)
ans =
    0.1760
>> normpdf(1,0,2)
ans =
    0.1760
```
    
2.)
```Bash
function [t] = untitled2(Megg,c,roe,K,Toriginal,Tboil,Tcenter)
Half1 = ((Megg^(2/3))*c*(roe^(1/3)))/(K*(pi^2)*(((4*pi)/3)^(2/3)));
Half2 = log(0.76*((Toriginal-Tboil)/(Tcenter-Tboil)));
t = Half1*Half2;
end

>> untitled2(67,3.7,1.038,0.0054,4,100,70)
ans =
  396.5763
>> untitled2(67,3.7,1.038,0.0054,20,100,70)
ans =
  315.2179
```
  
  3.)
```Bash
function [outputPolarStruct] = getPolar(inputCartesianStruct)
checkx = isfield(inputPolarStruct,'x');
checky = isfield(inputPolarStruct,'y');
if checkx == checky == 1 
outputPolarStruct.r = sqrt((inputCartesianStruct.x^2)+(inputCartesianStruct.x^2));
outputPolarStruct.phi = acos(inputCartesianStruct.x/outputPolarStruct.r);
else
disp('Please check your input fields');
end
```
```Bash
function [outputCartesianStruct] = getCart(inputPolarStruct)
checkr = isfield(inputPolarStruct,'r');
checkphi = isfield(inputPolarStruct,'phi');
if checkr == checkphi == 1 
outputCartesianStruct.x = inputPolarStruct.r*cos(inputPolarStruct.phi);
outputCartesianStruct.y = inputPolarStruct.r*sin(inputPolarStruct.phi);
else
disp('Please check your input fields');
end
```

4.)
```Bash
function [bytes] = getSize(x)
s = dir(x);
z = size(s);
bytes = 0;
for c = 1:z(1,1)
    bytes = bytes + s(c).bytes;
end
end
```

5.)
```Bash
function [] = fib()
again=1;
while again == 1
    z = input('Please enter a non-negative integer or type stop: ', 's');
    if strcmp(z,'stop') == 1
    again=0;
    else
    z = str2double(z);
        if isreal(z)==1 && z==round(z) && z>=0
          y = getFib(z);
          fprintf('fib(%d) = %d\n', z, y)
        else
          disp('The input argument is not a non-negative integer!')
        end
    end
end
```
```Bash
function [y] = getFib(n_int)
if n_int == 0
    y = 0;
elseif n_int == 1
    y = 1;
else
    y = getFib(n_int-1)+getFib(n_int-2);
end
end
```

6.)
```Bash
function [area] = getTriangleArea(vertices)
area = .5*((vertices(2,1)*vertices(3,2))-(vertices(3,1)*vertices(2,2))-(vertices(1,1)*vertices(3,2))+(vertices(3,1)*vertices(1,2))+(vertices(1,1)*vertices(2,2))-(vertices(2,1)*vertices(1,2)));
end
```

7.)
```Bash
function f = isPrime(n)
    if n < 0
    disp('Prime numbers are only defined for positive integers')
    else
    f = prime(n,n-1);
    end
      function p = prime(n,d)
        if n<= 2
            p = true;
        elseif d == 1
            p = true;
        elseif mod(n,d)==0
            p = false;
        else
            p = prime(n,d-1);
        end
    end
end
```
