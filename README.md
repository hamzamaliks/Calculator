# Calculator

Introduction:

Calculators are a big help when doing mathematical equations correctly. They are also a useful tool in learning different ways to do mathematics. The use of them plays a big part in excelling in math.

Methodology:

We will use the concepts of assembly language that we have learnt in COAL Lab.

We will use emu8086 as a compiler in this project.

Operations:

We have make various operations in our Calculator.

1.	Addition
2.	Multiplication
3.	Subtraction
4.	Division
5.	Cube
6.	Square

Code:

org 100h

include emu8086.inc
.data
a dw ?
num1 dw ?   ;FIRST OPERAND
num2 dw ?   ;SECOND OPERAND
result  dw ?
.code


printn

print '<<<<+-*/WELCOME+-*/>>>>'
printn
printn
printn
print '<<<<CODE BY 200901057 , 200901060>>>>>'
printn
printn
 


printn
printn
print '<<<<<<What Operation You Want To Perform:>>>>>>> '
printn
printn                                     ;OPERATIONS TO BE PERFORMED

print '1>> Addition (+) '
printn
printn

print '2>> Multiplication(*) '
printn
printn

print '3>> Subtraction (-) '
printn
printn

print '4>> Division (/) '
printn
printn
 
print '5>> Square (^2) '
printn
printn

print '6>> Cube (^3) ' 
printn
printn

print '7>> Exit'
printn
printn

print '                 Note:Integers Value only'


start:
printn
printn
print '>> Press Any Number From The Above Given List :'


call scan_num
mov a,cx
mov ax,a

printn                              
;COMPARE THE ENTERED NUMBER WITH THE FOLLOWING CONDITIONS
;JUMP TO THE ENTERED CONDITION 

cmp ax,1
je addition

cmp ax,2
je multiplication

cmp ax,3
je subtraction

cmp ax,4
je division

cmp ax,5
je square

cmp ax,6
je cube  


cmp ax,7
je exit

ADDITION 
addition:
 
printn
print '++++++++ADDITION++++++ '        ; PERFORMING ADDITION
printn 
printn
print '>> Enter First Number: '          ;FIRST OPERAND
call scan_num
mov num1,cx
mov ax,num1
printn

print '>> Enter Second Number: '         ;SECOND OPERAND
call scan_num
mov num2,cx
mov bx,num2

printn
add ax,bx 

print '>> Result: '                      ;RESULT
call print_num

jmp start:
MULTIPLICATION
 multiplication:

printn
print '******MULTIPLICATION******* '     ; PERFORMING MULTIPLICATION
printn
printn

print '>> Enter First Number: '                ;FIRST OPERAND
call scan_num
mov num1,cx
mov ax,num1
printn

print '>> Enter Second Number: '               ;SECOND OPERAND
call scan_num
mov num2,cx
mov bx,num2
printn

mul bx                                         ;RESULT
print '>> Result: '
call print_num
jmp start:

SUBTRACTION
subtraction:
printn
print '----------SUBTRACTION--------- '       ;PERFORMING SUBTRACTION
printn
printn
                                          
print '>> Enter First Number: '                 ;FIRST OPERAND
call scan_num
mov num1,cx
mov ax,num1
printn

print '>> Enter Second Number: '                ;SECOND OPERAND
call scan_num
mov num2,cx
mov bx,num2
printn

sub ax,bx
print '>> Result: '                             ;RESULT
call print_num 

jmp start:
DIVISION
division:
printn
print '////////DIVISION///////////'             ;PERFORMING DIVISION
printn

print '>> Enter First Number: '                   ;FIRST OPERAND
call scan_num
mov num1,cx
mov ax,num1
printn

print '>> Enter Second Number: '                  ;SECOND OPERAND
call scan_num
mov num2,cx
mov bx,num2
printn

div bx
PRINT '>> Result: '                               ;RESULT
call print_num

jmp start:
 



SQUARE

square:

printn
print '^2^2^2^2 SQUARE ^2^2^2^2 '                   ;PERFORMING SQUARE
printn
printn 

print '>> Enter The Number: '                        ;OPERAND
call scan_num
mov num1,cx
mov ax,num1
printn 

mul ax
print '>> Result: '
call print_num                                       ;RESULT

jmp start:
CUBE
cube:
printn
print '^3^3^3^3 CUBE ^3^3^3^3'                      ;PERFORMING CUBE
printn
printn 

print '>> Enter The Number: '                        ;OPERAND
call scan_num
mov num1,cx
mov ax,num1
printn 

mul num1
mov result,ax
mul num1

print '>> Result: '                                  ;RESULT
call print_num

jmp start:
 
EXIT

exit:
                                               ;EXIT   
printn

print '<<<<<<+-*/! GOOD BYE !+-*/>>>>> '   
printn
DEFINE_SCAN_NUM
DEFINE_PRINT_NUM
DEFINE_PRINT_NUM_UNS 

Ret
OUTPUT
Main Menu 
 
 ![image](https://user-images.githubusercontent.com/114498003/193596483-28fa83fd-b8b0-4cbc-bd24-1646690a2d32.png)

ADDITION 

![image](https://user-images.githubusercontent.com/114498003/193596532-d34c2eef-867a-4b66-8554-24d46fe6fcd3.png)

 
SUBTRACTION
 
 ![image](https://user-images.githubusercontent.com/114498003/193596573-514f7d27-c5e8-4046-bcfc-ce45ba9ee177.png)





MULTIPLICATION

![image](https://user-images.githubusercontent.com/114498003/193596614-3504ad53-fd22-4bff-b311-5273530e4697.png)

 
DIVISION

![image](https://user-images.githubusercontent.com/114498003/193596739-89d8b3d2-bb88-43c5-b943-63da214142a5.png)

 
SQUARE

![image](https://user-images.githubusercontent.com/114498003/193596783-9cb5e3f4-37c5-4507-8324-45fa3d665ae0.png)

 
CUBE

![image](https://user-images.githubusercontent.com/114498003/193596823-998dc312-2c3d-4ffb-9e95-4a19ea359ccd.png)

 
GOODBYE 
 
 ![image](https://user-images.githubusercontent.com/114498003/193596857-bf1ed98f-6062-42a9-b62c-e3aa6aeee73d.png)





