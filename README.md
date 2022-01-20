# H-
酒店管理系统
package com.home;

import java.util.Scanner;

public class hotl {
    private Room[][] rooms;
	//hotl无参构造方法创建hotl对象是自动调用此方法
    public hotl() {
    //初始化酒店的房间（二维数组的遍历以及动态初始化）
        rooms = new Room[3][6];
        for (int i = 0; i < rooms.length; i++) {
            for (int j = 0; j < rooms[i].length; j++) {
                Room rn = new Room();
                rn.setRid((100 * (i + 1) + j + 1));
                if (i == 0) {
                    rn.setType("单人人间");
                } else if (i == 1) {
                    rn.setType("双人人间");
                } else if (i == 2) {
                    rn.setType("总统套房");
                }
                rooms[i][j] = rn;
            }
        }
    }
	//打印酒店每个房间（二维数组的遍历）
    public void PrintRooms() {
        for (int i = 0; i < rooms.length; i++) {
            for (int j = 0; j < rooms[i].length; j++) {
                System.out.print(rooms[i][j] + " ");
            }
            System.out.println(" ");
        }
        System.out.println("查看所有房间成功"+"请继续输入数字指令");
    }
	//订房
    public void setRooms() {
        System.out.println("请输入你要入住的房间号");
        Scanner sc = new Scanner(System.in);
        int id = sc.nextInt();
        Room rn = rooms[id / 100 - 1][id % 100 - 1];
        rn.setZt(true);
        System.out.println("订房成功你的房间号为"+id+"请继续输入数字指令");
    }
	//退房
    public void EscRooms() {
        System.out.println("请输入你要退住的房间号");
        Scanner sc = new Scanner(System.in);
        int id = sc.nextInt();
        Room rn = rooms[id / 100 - 1][id % 100 - 1];
        rn.setZt(false);
        System.out.println("退房成功你退的房间号为"+id+"请继续输入数字指令");
    }

   
}

