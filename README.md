# EXPERIMENT-01: BUILDING LOGICAL CIRCUITS

## 1. Aim

To design, implement, simplify, and verify combinational logic circuits using Boolean algebra and digital logic gates.

## 2. Boolean Notation

Use the following notation throughout this experiment:

| Symbol | Meaning | Example |
|---|---|---|
| `!A` | NOT A | `!A` |
| `A & B` | AND | `A & B` |
| `A \| B` | OR | `A \| B` |
| `A ^ B` | XOR | `A ^ B` |
| `A XNOR B` | XNOR | `A XNOR B` |

**Important:** In these equations, `!` means NOT, `&` means AND, `|` means OR, and `^` means XOR. Parentheses determine the order of operations.

## 3. Advanced Boolean Equations

### Equation 1: Four-Input Sum-of-Products

```text
F1 = (!A & B & C)
   | (A & B & !D)
   | (!B & C & D)
   | (A & !C & D)
```

**Inputs:** A, B, C, D  
**Output:** F1  
**Challenge:** Simplify the expression and compare gate counts.

### Equation 2: Product-of-Sums Circuit

```text
F2 = (A | !B | C)
   & (!A | B | D)
   & (B | !C | !D)
```

**Inputs:** A, B, C, D  
**Output:** F2  
**Challenge:** Implement the circuit using NAND gates and verify functional equivalence.

### Equation 3: Nested Complement Logic

```text
F3 = !(
       ((! (A | B)) | (C & D))
       &
       (A | (!(B | C)))
     )
```

**Inputs:** A, B, C, D  
**Output:** F3  
**Challenge:** Apply De Morgan's theorems and implement the circuit using NAND and NOR gates.

### Equation 4: XOR-XNOR Combinational Circuit

```text
F4 = ((A XOR B) & (C XNOR D))
   | (!A & B & (C XOR D))
```

**Inputs:** A, B, C, D  
**Output:** F4  
**Challenge:** Compare an XOR/XNOR implementation with a basic-gate implementation.

### Equation 5: Five-Input Logic Function

```text
F5 = (A & B & !C)
   | (!A & D & E)
   | (B & C & !E)
   | (!B & C & D)
```

**Inputs:** A, B, C, D, E  
**Output:** F5  
**Challenge:** Generate and verify all 32 input combinations.

### Equation 6: Six-Input Mixed Logic

```text
F6 = ((A | B) & !(C | D))
   | ((C XOR E) & (D | G))
   | (!A & B & E)
```

**Inputs:** A, B, C, D, E, G  
**Output:** F6  
**Challenge:** Calculate gate count and logic depth. Verify all 64 input combinations.

### Equation 7: NAND-NOR Hybrid Logic

```text
F7 = (! (A & B) & !(C | D))
   | (!(A | C) & B & D)
```

**Inputs:** A, B, C, D  
**Output:** F7  
**Challenge:** Implement the function using NAND and NOR gates with any required input inversions.

### Equation 8: Six-Input Advanced Combinational Logic

```text
F8 = ((A XOR B) & (C XNOR D))
   | (!(A | B) & C & E)
   | (A & B & !(D | F))
```

**Inputs:** A, B, C, D, E, F  
**Output:** F8  
**Challenge:** Simplify the expression, design the circuit, and verify all 64 input combinations.

## 4. Experimental Procedure

1. Identify all input variables and the output.
2. Draw the logic circuit for each equation.
3. Implement the circuit in Logisim Evolution, Proteus, or a digital logic trainer kit.
4. Apply all possible input combinations.
5. Record the expected and observed outputs.
6. Simplify the Boolean expression using Boolean algebra.
7. Build the simplified circuit and compare gate counts.
8. Save the circuit diagrams, truth tables, and verification screenshots.

## 5. Truth Table Requirements

| Number of inputs | Required combinations |
|---:|---:|
| 4 | 16 |
| 5 | 32 |
| 6 | 64 |

Use this format to record the results:

| Inputs | Expected output | Observed output | Status |
|---|---|---|---|
| 0000 |  |  |  |
| 0001 |  |  |  |
| 0010 |  |  |  |
| ... |  |  |  |

Extend the table to include every input combination required by each equation.

## 6. Performance Analysis

For each circuit, record:

- Number of AND gates
- Number of OR gates
- Number of NOT gates
- Number of XOR/XNOR gates
- Total gate count
- Logic depth
- Functional equivalence before and after simplification

## 7. Expected Results (drop the screenshots of each equations circuit )
F1 = (!A & B & C) | (A & B & !D) | (!B & C & D) | (A & !C & D) Shown with inputs A=0, B=0, C=1, D=1  ->  F1 = 1

F2 = (A | !B | C) & (!A | B | D) & (B | !C | !D) Shown with inputs A=0, B=0, C=0, D=0  ->  F2 = 1

F3 = !( ((!(A | B)) | (C & D)) & (A | (!(B | C))) ) Shown with inputs A=0, B=0, C=1, D=0  ->  F3 = 1

F4 = ((A XOR B) & (C XNOR D)) | (!A & B & (C XOR D)) Shown with inputs A=0, B=1, C=0, D=0  ->  F4 = 1

F5 = (A & B & !C) | (!A & D & E) | (B & C & !E) | (!B & C & D) Shown with inputs A=0, B=0, C=0, D=1, E=1  ->  F5 = 1

F6 = ((A | B) & !(C | D)) | ((C XOR E) & (D | G)) | (!A & B & E) Shown with inputs A=0, B=0, C=0, D=0, E=1, G=1  ->  F6 = 1

F7 = (!(A & B) & !(C | D)) | (!(A | C) & B & D) Shown with inputs A=0, B=0, C=0, D=0  ->  F7 = 1

F8 = ((A XOR B) & (C XNOR D)) | (!(A | B) & C & E) | (A & B & !(D | F)) Shown with inputs A=0, B=0, C=1, D=0, E=1, F=0  ->  F8 = 1


Screenshorts:
<img width="2082" height="1149" alt="EX1" src="https://github.com/user-attachments/assets/745fba2a-863c-44ab-8b5a-1c7299f6981b" />
<img width="2152" height="960" alt="EX2" src="https://github.com/user-attachments/assets/9de8c0e0-f64f-464c-84bb-542c74806062" />
<img width="1417" height="652" alt="EX3" src="https://github.com/user-attachments/assets/393e58df-a787-419f-a23f-eeee199c7389" />
<img width="1047" height="530" alt="EX4" src="https://github.com/user-attachments/assets/f2e9fa29-50d4-4d7c-9c3a-b816cbffcad2" />
<img width="1326" height="650" alt="EX5" src="https://github.com/user-attachments/assets/24d8df00-dc42-402e-a638-0a3aa17ce1fc" />
<img width="1153" height="625" alt="EX6" src="https://github.com/user-attachments/assets/bc7e00fd-76ab-46b9-a220-2d41eb799e79" />
<img width="1056" height="582" alt="EX7" src="https://github.com/user-attachments/assets/dbd4c153-4d16-4f5e-8cc9-8fd755695559" />
<img width="1302" height="652" alt="EX8" src="https://github.com/user-attachments/assets/64cd36a6-1830-48ed-a88a-e5f85fcec433" />


 
## 8. Result

The logic circuits are designed, implemented, and verified using Boolean algebra and digital logic gates. The original and simplified circuits are compared based on gate count and logic depth.
 
 
