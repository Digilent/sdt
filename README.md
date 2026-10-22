# Generated System Device Tree(SDT) for Zynq Ultarscale+ MPSoCs

## To generate new SDT source `Vivado/settings.sh` then:

```bash
rm -rf sdt && sdtgen -xsa ./hw/system_wrapper.xsa -dir ./sdt -user_dts <list of .dtsi files separade by space>
```

## Import into yocto


```bash
export PATH=$PATH:/path/to/meta-xilinx/gen-machine-conf
gen-machine-conf parse-sdt --template </path/to/cancun.yaml>
```

## For gensys zu

### Generate SDT

```bash
rm -rf sdt/ && sdtgen -xsa ./hw/design_1_wrapper.xsa -dir ./sdt -user_dts genesyszu.dtsi genesyszu-5ev.dtsi
```

### Import in yocto
```bash
export PATH=$PATH:/<path/to/layers/>/meta-xilinx/gen-machine-conf
gen-machine-conf parse-sdt --template ../sdt/genesyszu-5ev.yaml
```

