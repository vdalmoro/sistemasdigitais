module somador(input clock,
	input [31:0] E1,
	input [31:0] E2,
	output[31:0] OUT);
	
  assing OUT = saida;
	reg [31:0] soma = 0;
	reg [31:0] saida = 0;
	always @(posedge clock) begin
		soma <= E1 + E2;
		saida = soma + saida; 
	end
endmodule

module teste; 
	reg CLK_50;
	reg[31:0] E1, E2;
	wire[31:0] OUT;
	always clock = ~clock;
	somador (clock, E1, E2, S0);
	initial begin
		$dumpvars();
    #0
		CLK_50 <= 0;
		E1 <= 1;
		E2 <= 1;
		//2
		#8
		E1 <= 3;
		E2 <= 3;
		//8
		#8
		E1 <= 5;
		E2 <= 5;
		//18
		#8
		$finish;
	end
endmodule
