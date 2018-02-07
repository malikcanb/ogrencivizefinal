package diziler;

import java.util.Scanner;

public class or1 {

	public static void main(String[] args) {
		Scanner klavye=new Scanner(System.in);
		System.out.println("kişi sayısını giriniz0");
		byte ks = klavye.nextByte();
		String ad[] = new String[ks];
		byte vize[]= new byte[ks];
		byte finalnot[]=new byte[ks];
		byte i;
		byte bn[]=new byte[ks];
		int vt=0, ft=0,bt=0,vo,fo,bno=0;
		for(i=0;i<ks;i++) {
			System.out.println("isim giriniz");
			ad[i]= klavye.next();
			System.out.println("Vize giriniz");
			vize[i]=klavye.nextByte();
			System.out.println("final giriniz");
			finalnot[i]=klavye.nextByte();
			bn[i]=(byte)((vize[i]+finalnot[i])/2);
			System.out.println("başarı notunuz" +bn[i]);
			vt+=vize[i];
			ft+=finalnot[i];
			bno = bno + bn[i];
		}
		vo= vt/ks;
		fo=ft/ks;
		bno=bno/bn.length;
		System.out.println("Vize ortalaması"+vo);
		System.out.println("final ortalaması"+fo);
		System.out.println("başarı not oralaması"+bno);
		for(i=0; i<ks;i++) {
			if(bn[i]>=bno) {
				System.out.println("\n"+i+"Kişinin bilgileri");
				System.out.println("isminiz"+ad[i]);
				System.out.println("vize notu"+vize[i]);
				System.out.println("final notunuz" +finalnot[1]);
				System.out.println("başarı notu"+bn[i]);
			}
		}
	}
}
