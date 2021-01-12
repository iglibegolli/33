# 33
.data
x: .word 4711
y: .word 13
z: .word 0 xA8F
e: .word 0
.text
.globl main
main :
lw x5, x
lw x6, y
lw x7, z
add x5, x5, x6
sub x6, x5, x7
sw x6, e , x5
#Exit by issuing a systemcall
li x17, 10
ecall
