var
i,n:integer; 
F:boolean;
procedure Simple(a:longint;var P:boolean);
var 
j:longint;
begin
P:=true; if a=1 then P:=false;
for j:=2 to a div 2 do
if a mod j =0 then P:=false;
end;
begin
writeln(&#39;n?&#39;);
readln(n);
for i:=1 to n do
begin
Simple(I,F)
if F then write(i,&#39;,&#39;);
end
end.



var
i,n:integer; F:boolean;
procedure Pol(a:longint;var P:Boolean);
var b,c:longint;
begin
b:=a; c:=0;
while b&gt;0 do
begin
c:=c*10+b mod 10; b:=b div 10;
end;
if a=c then P:=true else P:=false;
end;
begin
writeln(&#39;n?&#39;); 
readln(n);
for i:=10 to n do
begin Pol(i,F); if F then write(i,&#39;,&#39;) end;
end.


var
i,n:integer;
Procedure Perfect(a:longint;var P:boolean);
var S,j:longint;
begin
S:=0;
for j:=1 to a div 2 do
if a mod j=0 then s:=s+j;
if a=s then P:=true
else P:=false;
end;
begin writeln(&#39;n?&#39;); readln(n);
for i:=1 to n do
begin Perfect(I,F); if F then write(i,&#39;,&#39;) end;
end.



VAR
n,i:longint;
Function Roz(a:longint):byte;
VAR
k:byte;
BEGIN
k:=0;
While a&gt;0 do
BEGIN
a:=a div 10;
k:=k+1;
END;
Roz:=k;
END;
Function St10(m:byte):longint;
VAR
y:longint;
j:byte;
BEGIN
y:=1;
For j:=1 to m do
y:=y*10;
St10:=y;
END;
Function Avto(x:longint):boolean;
VAR
k:byte;
BEGIN
Avto:=false;
k:=Roz(x);
if x=Sqr(x) mod St10(k) then
Avto:=true;
END;
BEGIN
Writeln(&#39;Vvedite Chislo&#39;);
Readln(n);
For i:=1 to n do
If Avto(i) then Write(i,&#39;, &#39;);
Readln
END.



VAR
n,i:longint;
Function Roz(a:longint):byte;
VAR
k:byte;
BEGIN
k:=0;
While a>0 do
BEGIN
a:=a div 10;
k:=k+1;
END;
Roz:=k;
END;
Function St10(m:byte):longint;
VAR
y:longint;
j:byte;
BEGIN
y:=1;
For j:=1 to m do
y:=y*10;
St10:=y;
END;
Function L(x:longint):boolean;
VAR
k:byte;
d,xl,xr:longint;
BEGIN
L:=false;
k:=Roz(x);
If k mod 2=0 then
BEGIN
d:=St10(k div 2);
xl:=x div d;
xr:=x mod d;
If x=xl*xl+xr*xr then L:=true;
END;
END;
BEGIN
Writeln(&#39;Vvedite Chislo&#39;);
Readln(n);
For i:=10 to n do If L(i) then Write(i,&#39;, &#39;);
Readln
END.






VAR
n,i:longint;
Function Roz(a:longint):byte;
VAR
k:byte;
BEGIN
k:=0;
While a>0 do
BEGIN
a:=a div 10;
k:=k+1;
END;
Roz:=k;
END;
Function St(v,m:byte):longint;
VAR
y:longint;
j:byte;
BEGIN
y:=1;
For j:=1 to m do
y:=y*v;
St:=y;
END;
Function Arm(x:longint):boolean;
VAR
k,c:byte;
s,b:longint;
BEGIN
Arm:=false;
k:=Roz(x);
b:=x;
s:=0;
while b&gt;0 do
BEGIN
c:=b mod 10;
s:=s + st(c,k);
b:=b div 10;
END;
If s=x then Arm:=true;
END;
BEGIN
Writeln(&#39;Vvedite Chislo&#39;);
Readln(n);
For i:=10 to n do
If Arm(i) then Write(i,&#39;, &#39;);
Readln
END.

VAR
n,i:longint;
Function Roz(a:longint):byte;
VAR
k:byte;
BEGIN
k:=0;
While a&gt;0 do
BEGIN
a:=a div 10;
k:=k+1;
END;
Roz:=k;
END;
Function St10(m:byte):longint;
VAR
y:longint;
j:byte;
BEGIN
y:=1;
For j:=1 to m do
y:=y*10;
St10:=y;
END;
Function Sum(a:longint):byte;
VAR
S:byte;
BEGIN
S:=0;
While a&gt;0 do
BEGIN
S:=S+a mod 10;
a:=a div 10;
END;
Sum:=S;
END;
Function Lucky(x:longint):boolean;
VAR
k:byte;
d,xl,xr:longint;
BEGIN
Lucky:=false;
k:=Roz(x);
If k mod 2=0 then
BEGIN
d:=St10(k div 2);
xl:=x div d;
xr:=x mod d;
If Sum(xl)=Sum(xr) then
Lucky:=true;
END;
END;
BEGIN
Writeln(&#39;Vvedite Chislo&#39;);
Readln(n);
For i:=10 to n do
If Lucky(i) then Write(i,&#39;, &#39;);
Readln
END.

