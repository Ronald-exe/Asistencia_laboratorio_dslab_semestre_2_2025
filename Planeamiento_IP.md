# 1. IP design in Vivado...

## Step 1:
I have to use the IP tools in vivado, after select the distributed Memory  Generator.
![IP_Tool](https://github.com/Ronald-exe/Asistencia_laboratorio_dslab_semestre_2_2025/blob/main/fig/Select_IP.png)

## Step 2:
We choose between ROM or Single_RAM_Port
![ROM_RAM](https://github.com/Ronald-exe/Asistencia_laboratorio_dslab_semestre_2_2025/blob/main/fig/choose_between_ROM_RAM.png)

## Step 3:
ROM code.......
```verilog
    dist_mem_gen_0_ROM ROM (
        .a                  (rom_addr[10:2]),
        .spo                (rom_instr)
    );
```

RAM code.......
```verilog
    dist_mem_gen_0_RAM RAM  (
        .clk                (clk_i),
        .we                 (we_ram),
        .a                  (addr_ram),
        .d                  (write_ram),
        .spo                (data_ram)
    );
```



