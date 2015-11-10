# hadoop
Hadoop 常用参数
参数名称
说明
stream.memory.limit	单个map，reduce最高使用内存,默认800M
mapred.map.memory.limit	单个map最高使用内存，优先级高于stream.memory.limit
mapred.reduce.memory.limit	单个reduce最高使用内存，优先级高于stream.memory.limit
mapred.map.capacity.per.tasktracker	每台机器最多同时启动map个数
mapred.reduce.capacity.per.tasktracker	每台机器最多同时启动reduce个数
mapred.job.map.capacity	map并发数目
mapred.job.reduce.capacity	reduce并发数目
abaci.job.map.max.capacity	map并发限制，默认10000
abaci.job.reduce.max.capacity	reduce并发限制，默认3000
mapred.map.tasks	map数目
mapred.reduce.tasks	reduce数目
mapred.job.reuse.jvm.num.tasks	1表示不reuse，-1表示无限reuse，其他数值表示每个jvm reuse次数。reuse的时候，map结束时不会释放内存！
mapred.compress.map.output	指定map的输出是否压缩。有助于减小数据量，减小io压力，但压缩和解压有cpu成本，需要慎重选择压缩算法。
mapred.map.output.compression.codec	map输出的压缩算法
mapred.output.compress	结果输出是否压缩
mapred.output.compression.codec	控制mapred的输出的压缩的方式
io.compression.codecs	压缩算法
mapred.max.map.failures.percent	容忍map错误百分比，默认为0
mapred.max.reduce.failures.percent	容忍reduce错误百分比，默认为0
stream.map.output.field.separator	map输出分隔符，默认Tab
stream.reduce.output.field.separator	reduce输出分隔符，默认Tab
mapred.textoutputformat.separator	设置TextOutputFormat的输出key,value分隔符，默认Tab
mapred.textoutputformat.ignoreseparator	设置为true后，当只有key没有value会去掉自动补上的Tab
mapred.min.split.size	指定map最小处理数据量，单位B
mapred.max.split.size	指定map最多处理数据量，单位B，同时设置inputformat=org.apache.hadoop.mapred.CombineTextInputFormat
mapred.combine.input.format.local.only	是否只合并本节点，默认true，设置为false可以跨节点合并数据
abaci.job.map.cpu.percent	map消耗cpu占比，参数默认值40（表示1个cpu的40%，即0.4个cpu）
abaci.job.reduce.cpu.percent	reduce消耗cpu占比，参数默认值40（表示1个cpu的40%，即0.4个cpu）
mapred.map.capacity.per.tasktracker	表示每个节点最多并行跑几个该job的map任务（请根据内存情况适当增减该参数，默认是8）
mapred.reduce.capacity.per.tasktracker	表示每个节点最多并行跑几个该job的reduce任务（请根据内存情况适当增减该参数，默认是8）
mapred.map.tasks.speculative.execution	开启map预测执行，默认true
mapred.reduce.tasks.speculative.execution	开启reduce预测执行，默认true
mapred.textoutputformat.ignoreseparator	当只输出key的时候是否忽略末尾的Tab分隔符，默认false， 设置为true只输出key的内容
