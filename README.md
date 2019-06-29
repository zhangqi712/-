的#include <stdio.h>中 
的#include <stdlib.h>中
的#include <string.h>的


结构数据

{ 
int金额; //数量
char name [20]; //名称
int num; //编号
char nature [15]; //属性
char备注[50]; //备注
浮动价格; //价格
}食品[100];

int S = 0; //货物数

//入库函数
int i = 0;
void input（） 
 { 

char c; 
而（1） 
{ 
系统（ “CLS”）; 
的printf（ “元件物品％d \ n” 个，++ S）; 
的printf（ “请输入元件物品编号：”）; 
的scanf（ “％d”，＆食品[I] .num）; 
的printf（ “请输入元件物品名称：”）;
的scanf（ “％S”，＆食品[I]。名称）;  
的printf（ “请输入元件物品属性（15个字以内）：”）; //
的scanf（ “％S”，食品[I] .nature）;
的printf（ “请输入元件物品价格：”）;
的scanf（ “％F”，＆食品[I]。价格）;

的printf（ “请输入物品数量：”）; 
的scanf（ “％d”，＆食品[I] .amount）; 
的printf（ “请输入元件物品备注（50个字以内）：”）; //
的scanf（ “％S”，食品[I] .remarks）;
的printf（ “是否继续入库（Y / N）：”）; 
scanf（“％c”，＆c）; 
我++; 
如果（c =='N'|| c =='n'）中断; 
} 
 }

//出库函数

void output（） 
 { 
int a，b，c，i，j = 0; 
char _nature [10]; 
char d; 
char _name [20]; 
而（1） 
{ 
系统（ “CLS”）; 
的printf（ “\吨\ T1，按元件编号出库\ n”）; 
的printf（ “\吨\ T2，按元件名称出库\ n”）; 
的printf（ “\吨\ t3时，按元件属性出库\ n”）; 
的printf（ “\吨\ t0时，返回\ n”）; 
的printf（ “\吨\吨请选择：”）; 
的scanf（ “％d”，＆一个）; 
如果（一个== 1） 
{ 
的printf（ “请输入出货元件的编号：”）; 
的scanf（ “％d”，和b）; 
的printf（ “\ n”）; 
对于（I = 0; I <S;我++） 
{ 
if（b == food [i] .num）j = i; 
} 
如果（食品[j]的.amount> 0） 
{ 
的printf（ “请输入元件出货量：”）; 
的scanf（ “％d”，＆amp; C）; 
如果（C>食品[j]的.amount） 
的printf（ “元件货物不足\ n”）; 
其他 
{ 
食品[j]的.amount- = C; 
的printf（ “编号％d货物成功出货\ n货物剩余％d \ n！”，食品[J] .num，食品[j]的.amount）; 
} 
} 
其他 
{ 
的printf（ “此货物为零\ n”）; 
} 
} 
如果（A == 2） 
{ 
的printf（ “请输入出货货物的名称：”）; 
的scanf（ “％S”，_名称）; 
的printf（ “\ n”）; 
对于（I = 0; I <S;我++） 
{ 
if（strcmp（food [i] .name，_name）== 0）j = i; 
} 
如果（食品[j]的.amount> 0） 
{ 
的printf（ “请输入出货量：”）; 
的scanf（ “％d”，＆amp; C）; 
如果（C>食品[j]的.amount） 
的printf（ “货物不足\ n”）; 
其他 
{ 
食品[j]的.amount- = C; 
的printf（ “编号％d货物成功出货\ n货物剩余％d \ n！”，食品[J] .num，食品[j]的.amount）; 
} 
} 
其他 
{ 
的printf（ “此货物数量为零\ n”）; 
} 
} 
否则如果（a == 0）中断; 
的printf（ “是否继续出库（Y / N）：”）; 
scanf（“％c”，＆d）; 
if（d =='N'|| d =='n'）中断; 
} 
 } 

//货物出库和入库

void current（） 
 { 
int a; 
系统（ “CLS”）; 
的printf（ “\吨\ T1，货物入库\ n”）; 
的printf（ “\吨\ t2时，元件出库\ n”）; 
的printf（ “\吨\ t0时，返回\ n”）; 
的printf（ “\吨\吨请选择：”）; 
的scanf（ “％d”，＆一个）; 
如果（一个== 1） 
{ 
输入（）; 
} 
否则如果（a == 2） 
{ 
输出（）; 
} 
 }

//查找函数

void search（） 
 { 
int i，a，b; 
char c; 
char _name [20];
char _nature [10];
char _beizhu [50];
int item [100];
int flag = 0; 
而（1） 
{ 
系统（ “CLS”）; 
的printf（ “\吨\ T1，按元件编号查找\ n”）; 
的printf（ “\吨\ T2，按元件名称查找\ n”）; 
的printf（ “\吨\ t3时，按元件属性查找\ n”）; 
的printf（ “\吨\ t4时，按元件备注查找\ n”）; 
的printf（ “\吨\ t0时，返回\ n”）; 
的printf（ “\吨\吨请选择：”）; 
的scanf（ “％d”，＆一个）; 
如果（一个== 1） 
{ 
的printf（ “请输入需要查询元件的编号：”）; 
的scanf（ “％d”，和b）; 
的printf（ “\ n”）; 
对于（I = 0; I <S;我++） 
{ 
if（b == food [i] .num）break; 
} 
如果（I'S） 
的printf（ “编号：％d \ n名称：％S \ n数量：％d \ n” 个，食品[I] .num，食品[I] .name和食品[I] .amount）; 
其他 
的printf（ “未找到此编号\ n”）; 
printf（“是否继续查找（Y / N）：”）; 
scanf（“％c”，＆c）; 
如果（c =='N'|| c =='n'）中断; 
} 
否则如果（a == 2） 
{ 
的printf（ “请输入需要查询元件的名称：”）; 
的scanf（ “％S”，＆_名称）; 
的printf（ “\ n”）; 
对于（I = 0; I <S;我++） 
{ 
if（strcmp（_name，food [i] .name）== 0）break; 
} 
如果（I'S） 
的printf（ “编号：％d \ n名称：％S \ n数量：％d \ n” 个，食品[I] .num，食品[I] .name和食品[I] .amount）; 
其他 
的printf（ “未找到此名称\ n”）; 
printf（“是否继续查找（Y / N）：”）; 
scanf（“％c”，＆c）; 
如果（c =='N'|| c =='n'）中断; 
} 

否则如果（a == 3）
 {
 的printf（ “请输入需要查询元件的属性：”）;
 的scanf（ “％S”，_性质）;
 的printf（ “\ n”）;
 对于（I = 0; I <S;我++）
 {
 如果（的strcmp（_nature，食品[I] .nature）== 0）
 项[I] = 1;
 }
 对于（I = 0; I <S;我++）
 {
 
 如果（（项[I] == 1）&&（I <= S））
 {
 的printf（ “**************************** \ n”）;
 的printf（ “编号：％d \ n名称：％S \ n属性：％S \ n” 个，食品[I] .num，食品[I] .name和食品[I] .nature）;
 的printf（ “价格：％2F \ n数量：％d \ n备注：％S \ n” 个，食品[I]。价格，食品[I] .amount，食品[I] .remarks）;
 标志= 1;
 的printf（ “**************************** \ n”）;
 }
 
 }
 }
 否则如果（a == 4）
 {
 的printf（ “请输入需要查询元件的备注：”）;
 的scanf（ “％S”，_ beizhu）;
 的printf（ “\ n”）;
 对于（I = 0; I <S;我++）
 {
 如果（的strcmp（_beizhu，食品[I] .remarks）== 0）
 项[I] = 1;
 }
 对于（I = 0; I <S;我++）
 {
 
 如果（（项[I] == 1）&&（I <= S））
 {
 的printf（ “**************************** \ n”）;
 的printf（ “编号：％d \ n名称：％S \ n属性：％S \ n” 个，食品[I] .num，食品[I] .name和食品[I] .nature）;
 的printf（ “价格：％2F \ n数量：％d \ n备注：％S \ n” 个，食品[I]。价格，食品[I] .amount，食品[I] .remarks）;
 标志= 1;
 的printf（ “**************************** \ n”）;
 }
 
 }
 如果（标志== 0）
 的printf（ “未找到此属性的货物\ n”）;
 其他;
 printf（“是否继续查找（Y / N）：”）;
 scanf（“％c”，＆c）;
 如果（c =='N'|| c =='n'）中断;
 }
 否则如果（a == 0）中断;
 
 }
 
}



//显示函数

void show（） 
 { 
int i; 
char c; 
系统（ “CLS”）; 
printf（“\ t \ t编号\ t \ t名称\ t \ t属性\ t \ t价格\ t \ t数量\ t \ t备注\ n”）;
for（i = 0; i <S; i ++） 
{ 
 printf（“\ t \ t \ t％-16d％-16s％-16s”，food [i] .num，food [i] .name，food [i] .nature）;
 printf（“％16.2f％16d％16s”，food [i] .price，food [i] .amount，food [i] .remarks）;
 
 的printf（ “\ n”）;
} 
的printf（ “\ n \ n”）; 
的printf（ “按回车键返回！”）; 
C =的getchar（）; 
C =的getchar（）; 
 }

char文件[20]; //文件名，全局变量

//打开文件

void open（） 
 { 
FILE * fp; 
int i; 
char c; 
系统（ “CLS”）; 
的printf（ “输入打开的文件名：\ n”）; 
的scanf（ “％S”，文件）; 
如果（（FP = FOPEN（文件， “RB”））== NULL） 
{ 
printf（“无法打开infile \ n”）; 
} 
如果（的fread（S，的sizeof（int）的，1，FP）！= 1） 
{ 
如果（FEOF（FP）） 
{ 
FCLOSE（FP）; 
回归; 
} 
的printf（ “文件读取错误\ n！”）; 
} 
对于（I = 0; I <S;我++） 
{ 
if（fread（＆food [i]，sizeof（struct data），1，fp）！= 1） 
{ 
如果（FEOF（FP）） 
{ 
FCLOSE（FP）; 
回归; 
} 
的printf（ “文件读取错误\ n！”）; 
} 
} 
FCLOSE（FP）; 
的printf（ “文件打开成功\ n \ n！”）; 
的printf（ “按回车键返回！”）; 
C =的getchar（）; 
C =的getchar（）; 
 }

//输出到文件

void save（） 
 { 
FILE * fp; 
int i，a; 
char c; 
系统（ “CLS”）; 
的printf（ “1，储存\ n”）; 
的printf（ “2，另存为\ n”）; 
的printf（ “0，返回\ n”）; 
的printf（ “请选择：”）; 
的scanf（ “％d”，＆一个）; 
如果（一个== 1） 
{ 
如果（（FP = FOPEN（文件， “WB”））== NULL） 
{ 
printf（“无法打开文件\ n”）; 
} 
如果（的fwrite（＆S，的sizeof（int）的，1，FP）！= 1） 
{ 
的printf（ “写入文件错误\ n！”）; 
} 
对于（I = 0; I <S;我++） 
{ 
if（fwrite（＆food [i]，sizeof（struct data），1，fp）！= 1） 
{ 
的printf（ “写入文件错误\ n！”）; 
} 
} 
FCLOSE（FP）; 
的printf（ “！保存成功\ n \ n”）; 
的printf（ “按回车键返回！”）; 
C =的getchar（）; 
C =的getchar（）; 
} 
否则如果（a == 2） 
{ 
的printf（ “\ n文件名：”）; 
的scanf（ “％S”，文件）; 
如果（（FP = FOPEN（文件， “WB”））== NULL） 
{ 
printf（“无法打开文件\ n”）; 
} 
如果（的fwrite（＆S，的sizeof（int）的，1，FP）！= 1） 
{ 
的printf（ “写入文件错误\ n！”）; 
} 
对于（I = 0; I <S;我++） 
{ 
if（fwrite（＆food [i]，sizeof（struct data），1，fp）！= 1） 
{ 
的printf（ “写入文件错误\ n！”）; 
} 
} 
FCLOSE（FP）; 
的printf（ “！保存成功\ n \ n”）; 
的printf（ “按回车键返回！”）; 
C =的getchar（）; 
C =的getchar（）; 
} 
 }
 void tongji（）
{
 int qqq = 0;
 系统（ “CLS”）;
 的printf（ “输入你统计的功能：\ n”）;
 printf（“1：库元器件的总价值\ n”）;
 printf（“2：每月出库元件的总价值\ n”）;
 printf（“3：各类元件的消耗量\ n”）;
 的scanf（ “％d”，＆QQQ）;
 的printf（ “\ n”）;
 的printf（ “\ n”）;
 如果（QQQ == 1）
 {float zongjiazhi = 0;
 for（int i = 0; i <S; i ++）zongjiazhi + = food [i] .amount * food [i] .price;
 输出（ “总价值为％.2f \ n” 个，zongjiazhi）;
 的printf（ “按回车键返回！”）;
 的getchar（）;
 的getchar（）;
 }
 否则如果（qqq == 2）
 {
 
 的printf（ “\ n”）;
 float zongjiazhi = 0;
 for（int i = 0; i <S; i ++）
 {int shuliang = 0;
 的printf（ “请输上个月％s的物品的数量：”，食品[I]。名称）;
 的scanf（ “％d”，＆王树亮）;
 
 zongjiazhi + =王树亮*食品[I]。价格;
 }
 for（int i = 0; i <S; i ++）zongjiazhi- = food [i] .amount * food [i] .price;
 的printf（ “\ n”）;
 的printf（ “出库元器件的总价值％.2f \ n” 个，zongjiazhi）;
 的printf（ “按回车键返回！”）;
 的getchar（）;
 的getchar（）;
 }
 否则如果（qqq == 3）
 {
 的printf（ “请输入上个月各类元器件的库数量：\ n”）;
 的printf（ “\ n”）;
 int xiaohaoliang [100];
 for（int i = 0; i <S; i ++）
 {int shuliang = 0;
 的printf（ “请输入％s的物品的数量：”，食品[I]。名称）;
 的scanf（ “％d”，＆王树亮）;
 
 shuliang- =食品[I] .num;
 xiaohaoliang [I] =王树亮;
 
 }
 的printf（ “\ n”）; printf的（ “\ n”）; printf的（ “\ n”）; printf的（ “\ n”）;
 for（int i = 0; i <S; i ++）
 {
 的printf（ “％S消耗量为％d \ n” 个，食品[I] .name和xiaohaoliang [I]）;
 }
 的printf（ “\ n”）;
 的printf（ “按回车键返回！”）;
 的getchar（）;
 的getchar（）;
 
 }
}

int main（） 
 { 
int a; 
///主菜单 
而（1） 
{ 
系统（ “CLS”）; 
printf（“\ t \ t \ t \ t * * * * * * * * * * * * * * * * \ n”）; 
printf（“\ t \ t \ t \ t * 1，元件出库和入库* \ n”）; 
printf（“\ t \ t \ t \ t * 2，查找元件表* \ n”）; 
printf（“\ t \ t \ t \ t * 3，显示仓库元件表* \ n”）; 
printf（“\ t \ t \ t \ t * 4，输出到文件* \ n”）; 
printf（“\ t \ t \ t \ t * 5，打开文件* \ n”）; 
printf（“\ t \ t \ t \ t * 6，统计* \ n”）; 
printf（“\ t \ t \ t \ t * 0，退出* \ n”）; 
printf（“\ t \ t \ t \ t * * * * * * * * * * * * * * * * \ n”）; 
的printf（ “\吨\吨\吨\吨请选择：”）; 
的scanf（ “％d”，＆一个）; 
切换（a）中 
{ 
案例1：current（）; break; 
案例2：search（）; break; 
案例3：show（）; break; 
案例4：save（）; break; 
案例5：open（）; break;
案例6：同济（）;休息; 
case 0：退出（0）; 
} 
} 
返回0; 
 }
