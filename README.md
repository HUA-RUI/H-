# H-
酒店管理系统
package com.home;

public class Room {
    private int rid;
    private String type;
    private boolean zt;

    public Room() {
    }

    public Room(int rid, String type, boolean zt) {
        this.rid = rid;
        this.type = type;
        this.zt = zt;
    }

    public int getRid() {
        return rid;
    }

    public void setRid(int rid) {
        this.rid = rid;
    }

    public String getType() {
        return type;
    }

    public void setType(String type) {
        this.type = type;
    }

    public boolean isZt() {
        return zt;
    }

    public void setZt(boolean zt) {
        this.zt = zt;
    }

    @Override
    public String toString() {
        return "["+rid+type+(zt ? "占用" : "空闲")+"]";
    }
}

