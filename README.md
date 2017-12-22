# RGB-initial
making RGB initial data  for processing
function [RGB_Testdata] = RGBarray(Testdata)
[m,n] = size(Testdata);
RGB_Testdata = zeros(m,3*n);

for i =1:m
  for j=1:n
   for p =1:3 
 current = myhextorgb(char(Testdata(i,j,:))); 
    RGB_Testdata(i,3*(j-1)+p) = current(1,p);
   end
  end
end

end
