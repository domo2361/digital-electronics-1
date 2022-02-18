# Lab 1: Dominik Vaško

### De Morgan's laws

1. Equations of all three versions of logic function f(c,b,a):
![273515617_1017700625761674_7307085881935985619_n](https://user-images.githubusercontent.com/99724562/154660051-90d6f550-fb4f-45fe-b3f3-4380f3db38ea.jpg)


2. Listing of VHDL architecture from design file (`design.vhd`) for all three functions. Always use syntax highlighting, meaningful comments, and follow VHDL guidelines:

```vhdl
architecture dataflow of demorgan is
begin
    f_org_o  <= (not(b_i) and a_i) or (not(c_i) and not(b_i));
    f_nand_o <= ((b_i nand b_i) nand a_i) nand ((b_i nand b_i) nand (c_i nand c_i));
    f_nor_o  <= ((b_i nor (a_i nor a_i)) nor (c_i nor b_i)) nor ((b_i nor (a_i nor a_i)) nor (c_i nor b_i)); 
end architecture dataflow;
```

3. Complete table with logic functions' values:

| **c** | **b** |**a** | **f(c,b,a)_ORG** | **f(c,b,a)_NAND** | **f(c,b,a)_NOR** |
| :-: | :-: | :-: | :-: | :-: | :-: |
| 0 | 0 | 0 | 1 | 1 | 1 |
| 0 | 0 | 1 | 1 | 1 | 1 |
| 0 | 1 | 0 | 0 | 0 | 0 |
| 0 | 1 | 1 | 0 | 0 | 0 |
| 1 | 0 | 0 | 0 | 0 | 0 |
| 1 | 0 | 1 | 1 | 1 | 1 |
| 1 | 1 | 0 | 0 | 0 | 0 |
| 1 | 1 | 1 | 0 | 0 | 0 |

### Distributive laws

1. Screenshot with simulated time waveforms. Always display all inputs and outputs (display the inputs at the top of the image, the outputs below them) at the appropriate time scale!

   ![Snímka obrazovky 2022-02-18 112059](https://user-images.githubusercontent.com/99724562/154664068-85df48e8-fb61-4613-95c0-9926ea35a4be.png
)

2. Link to your public EDA Playground example:

   [my playground](https://www.edaplayground.com/x/5L92)
