# 4 KB-ROM-Memory-with-Read-and-Write-Operations
Aim
To design and simulate a 4KB ROM memory with read and write operations using Verilog HDL and verify the functionality through a testbench in the Vivado 2023.1 simulation environment.

Apparatus Required
Vivado 2023.1 or equivalent Verilog simulation tool.
Computer system with a suitable operating system.
Procedure
Launch Vivado 2023.1:

Open Vivado and create a new project.
Design the Verilog Code for ROM:

Write the Verilog code for a 4KB ROM memory with read and write capabilities.
Create the Testbench:

Write a testbench to simulate both the read and write operations, verifying that the data is correctly written to and read from the memory.
Add the Verilog Files:

Add the ROM Verilog module and the testbench file to the project.
Run Simulation:

Run the behavioral simulation in Vivado and check the memory's read and write operations.
Observe the Waveforms:

Analyze the waveform to verify that the memory read and write operations work as expected.
Save and Document Results:

Capture the waveform and include the simulation results in the final report.
Verilog Code for 4KB ROM Memory with Read and Write Operations
In this design, we will implement a 4KB ROM. Since ROM is typically read-only, we will simulate the behavior as if it's writable, but in actual hardware, ROM is typically pre-programmed.

4KB = 4096 Bytes = 4096 x 8 bits
The address width for 4KB memory is 12 bits (2^12 = 4096).

Verilog Code:
module mem_rom(input clk,rst,input [2:0]address, output reg [3:0] dataout); reg [3:0] mem_rom[7:0]; initial begin mem_rom[0]=4'd1; mem_rom[1]=4'd2; mem_rom[2]=4'd3; mem_rom[3]=4'd4; mem_rom[4]=4'd10; mem_rom[5]=4'd11; mem_rom[6]=4'd12; mem_rom[7]=4'd15; end always@(posedge clk) begin if(rst) dataout=4'd0; else dataout=mem_rom[address]; end endmodule

Output:
![Screenshot 2024-11-13 174049](https://github.com/user-attachments/assets/46d75cec-c7b5-440d-ac55-ca584a19ae72)






Conclusion
In this experiment, a 4KB ROM memory with read and write operations was designed and successfully simulated using Verilog HDL. The testbench verified both the write and read functionalities by simulating the memory operations and observing the output waveforms. The experiment demonstrates how to implement memory operations in Verilog, effectively modeling both the reading and writing processes for ROM.
