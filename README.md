# BPF
the BPF program

## bpf介绍
这部分提取来进程管理部分的指标，分别是过去一秒内的调度延迟、软中断时间、硬中断时间、特定进程的oncpu时间、就绪队列长度。

BTW:目前的代码是规定死的，不能自己配置任何选项，例如特定进程就可以使用argfarse模块完成，指标可以使用代码生成的方式。

## task和task_struct说明
这是一个提取进程描述符task_struct字段的小例子，数据存储在influxdb中，前端使用Grafana可视化工具展示数据