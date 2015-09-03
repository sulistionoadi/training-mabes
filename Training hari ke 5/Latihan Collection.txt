/*
 * To change this template, choose Tools | Templates
 * and open the template in the editor.
 */
package com.evaluasi1;

import com.evaluasi1.domain.User;
import java.util.ArrayList;
import java.util.Collections;
import java.util.HashMap;
import java.util.HashSet;
import java.util.Iterator;
import java.util.List;
import java.util.Map;
import java.util.Set;

/**
 *
 * @author AP
 */
public class LatihanCollections {
    public static void main(String[] args) {
        
        //------------LIST------------------------
        List lst = new ArrayList();
        
        lst.add("coba");
        lst.add(1);//harga
        lst.add(true);
        lst.add(2);//qty
        
        for (int i=0; i<lst.size(); i++){ //.size utk cek jumlah data listnya
            
            System.out.println("Data ke " + i + " = " + lst.get(i));
        }
        
        List<String> lstStr = new ArrayList<String>();
        lstStr.add("str1");
        lstStr.add("str2");
        System.out.println("---------------------------------------");
        for (String dtStr : lstStr) { 
        // String dari <String> / of String, dtStr variable dr lstStr.add, : lstStr nama listnya
            System.out.println("Data lstStr " + dtStr);
        }
        
        List<Integer> lstInt = new ArrayList<Integer>();
        lstInt.add(1);
        lstInt.add(3);
        lstInt.add(2);
        lstInt.add(4);
        lstInt.add(6);
        lstInt.add(5);
        lstInt.add(7);
        Collections.sort(lstInt); // untuk mengurutkan data list yang acak
        System.out.println("---------------------------------------------");
        for (Integer dtInt : lstInt) {
            System.out.println("Data Int " + dtInt);
        }
        
        Integer cek = 0;
        System.out.println("Apakah 3 ada di list ? " + lstInt.contains(cek));
        // Contains untuk cek apakah datanya ada di list
        
        List<User> users = new ArrayList<User>(); //list user diambil dari class user
        User user = new User(); // inisialisasi user baru /object baru
        user.setNama("joko"); //menset nama dari class user bisa jg set alamat, tergantung
        users.add(user); 
        
        user = new User();
        user.setNama("joni");
        users.add(user);
        
        
        for (User u : users){
            System.out.println("Nama user = " + u.getNama());
        }
        user = new User();
        user.setNama("joko");
        System.out.println("Apakah user " + user.getNama() + " ada ? " + users.contains(user));
        System.out.println("------------------------------");
        
        
        //---------MAP--------------------------
        Map mp = new HashMap();
        mp.put("key 1", "value 1");
        mp.put("key 2", "value 2");
        
        System.out.println("Isi map " + mp.size());
        System.out.println("Ambil nilai dari key1 = " + mp.get("key1"));
        
        for(Iterator it = mp.entrySet().iterator(); it.hasNext();){
            Map.Entry dtMap = (Map.Entry) it.next();
            System.out.println("Key = " + dtMap.getKey() + " value = " + dtMap.getValue());
        }
        
        mp = new HashMap();
        mp.put("key 3", "value 3");
        System.out.println("Apakah " + mp.values() + "ada ? " + mp.containsValue("value 3"));
        
        
        //------------SET------------------
        Set<Integer> setInt = new HashSet<Integer>();
        setInt.add(1);
        setInt.add(1);
        setInt.add(2);
        for (Integer dtSetInt : setInt) {
            System.out.println("dtSetInt " + dtSetInt);
        }
        
        Set<User> setusers = new HashSet<User>();
        User setuser = new User();
        setuser.setNama("agung");
        setusers.add(setuser);
        
        setuser = new User();
        setuser.setNama("agung");
        setusers.add(setuser);
        
        setuser = new User();
        setuser.setNama("Permana");
        setusers.add(setuser);
        
        for (User dtSetUser : setusers) {
            System.out.println("dtSetUser " + dtSetUser.getNama());
        }
              
    }
    
}
