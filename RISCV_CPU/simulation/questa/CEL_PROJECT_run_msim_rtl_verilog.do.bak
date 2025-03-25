transcript on
if {[file exists rtl_work]} {
	vdel -lib rtl_work -all
}
vlib rtl_work
vmap work rtl_work

vlog -vlog01compat -work work +incdir+C:/Users/benbt/Desktop/Comp_eng_lab_2/Final_Project/RISCV_CPU {C:/Users/benbt/Desktop/Comp_eng_lab_2/Final_Project/RISCV_CPU/cel_project.v}
vlog -sv -work work +incdir+C:/Users/benbt/Desktop/Comp_eng_lab_2/Final_Project/RISCV_CPU {C:/Users/benbt/Desktop/Comp_eng_lab_2/Final_Project/RISCV_CPU/riscvsingle.sv}

vlog -vlog01compat -work work +incdir+C:/Users/benbt/Desktop/Comp_eng_lab_2/Final_Project/RISCV_CPU {C:/Users/benbt/Desktop/Comp_eng_lab_2/Final_Project/RISCV_CPU/my_computer_tb.v}

vsim -t 1ps -L altera_ver -L lpm_ver -L sgate_ver -L altera_mf_ver -L altera_lnsim_ver -L fiftyfivenm_ver -L rtl_work -L work -voptargs="+acc"  my_computer_tb

add wave *
view structure
view signals
run -all
