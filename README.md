Test_Program
============

%%%%%%%    Testing out the site    %%%%%%%%%       

function [output_1 ] = Equation_test( medium,solution)
%UNTITLED Summary of this function goes here
%   Detailed explanation goes here


%%%%%%%%%    ERROR MESSAGES    %%%%%%%%%%%%%
  if medium<0
      fprintf('\nError:The first number of the sequence needs to be a positive number.\n\n')
  elseif solution<0
      fprintf('\nError:The second number of the sequence needs to be a positive number.\n\n')
  elseif medium>=solution
      fprintf('\nError:The first number of the sequence needs to be less than the second number of the sequence.\n\n')

 %%%%%%%%%%%%  Constants     %%%%%%%%%%%%%%%%%%%%%%
 PVC_Elbow=;
 PVC_Pipe_length=;
 PVC_Pipe_price=;
 Shelving=;
 
 Seed_price_pack=;      %assume 100 per pack
 
      
      
      
  %%%%%%%%%       Actual Calculations     %%%%%%%%%%%%%%%%%%
  else
      output_1=zeros(1,8);
      output_1(1,2)=solution;
      output_1(1,1)=medium;
      
      for i=3:8
        output_1(1,i)=output_1(1,i-1)+output_1(1,i-2);
      end
      
      fprintf('\nThe answer is %f \n',output_1);
  end
end
