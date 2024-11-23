## Part 1
1.D
2.首次适应性算法的空闲分区按地址由低到高进行排序，优先使用低址部分空闲区。
3.B
4.B
5.D
6.C
7.A
8.B


9.(1)页大小为 $2^{12}$ 字节，页表最大占用 $2^{20} \times 4 = 2^{22}$ 字节
(2)页目录号：`(LA >> 22) & 0x3ff`
页表索引：`(LA >> 12) & 0x3ff`
(3)
物理地址1: 0020 0020H 页框号1: 00900H
物理地址2: 0020 0024H 页框号2: 00901H
物理地址3: 0090 1000H


## Part 2
1.B
2.D
3.D
4.B
5.A
6.C
7.A
8.A

9.(1) $(3 + 1 + 1 + 1 + 1) / 12 = 58.3\%$
(2) $(3 + 3 + 2 + 1) / 12 = 75\%$

10.(1)数组的虚拟地址: 1080 1008H
页目录号: 042H
页号: 001H
页目录项的物理地址: 0020 1108H
页表项的物理地址: 0030 1004H
(2)在虚拟地址空间中必须连续，物理地址空间中不必须
(3)按行遍历局部性更好，数组按行优先存放，同一行的元素更会出现在一个页中，按行遍历可以降低页缺失率

11.(1) VPN: 36位;一级页表: 512项;TLBI: 5位
(2)64组; Tag: 36位; 组索引: 6位; 块内偏移: 6位
(3)VPO: 0x49B; TLBI: 0x8
(4)CT: 0x8048; CO: 0x1B