# Exp.No:35  
## TOWER OF HANOI

---

### AIM  
To write a Python program to implement **Tower of Hanoi** and display all the moves of the disks using a recursive function.  
Consider the names of the tower pegs as A, B, C. Get the number of disks value from the user.

---

### ALGORITHM  

1. **Start the program.**
2. **Input** the number of disks `n`.
3. **Print** the number of disks.
4. Define a **recursive function** `TowerOfHanoi(n, source, destination, auxiliary)`:
   - If `n == 1`:
     - Print: "Move disk from source to destination".
   - Else:
     - Call `TowerOfHanoi(n - 1, source, auxiliary, destination)`  
       → Move `n-1` disks from source to auxiliary using destination as helper.
     - Print: "Move disk from source to destination"  
       → Move the largest disk to the destination.
     - Call `TowerOfHanoi(n - 1, auxiliary, destination, source)`  
       → Move `n-1` disks from auxiliary to destination using source as helper.
5. Call `TowerOfHanoi(n, 'A', 'C', 'B')` to start the process.
6. **End the program.**

---

### PROGRAM  

```python
#REGNO:-212222060262
#Name:- SUJAN S B
def TowerOfHanoi(n , source, destination, auxiliary):
	
	if(n>0):
	    TowerOfHanoi(n-1, source, auxiliary,destination)
	    print("Move disk from",source,"to",destination)
	    TowerOfHanoi(n-1, auxiliary,destination,source)
n=int(input())		
print("No. of disks =",n)


```

### OUTPUT
<img width="945" height="838" alt="image" src="https://github.com/user-attachments/assets/a2c4dd5f-4916-4723-9b5b-b0adc733e4ba" />

### RESULT
Thus a Python program to implement Tower of Hanoi and display all the moves of the disks using a recursive function has been executed successfully.
