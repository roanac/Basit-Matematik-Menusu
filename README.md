# Basit-Matematik-Menusu
basit matematik işlemleri içeren kendi çapımdaki ilk projem
#include <stdio.h>
#include <stdlib.h>


int main() {
	
	//Denedigim ilk (bana gore) uzun satir sayisina sahip kod. kendimce basit matematik islemleri yapmaya calistim.
	
	int secim;
	int pi=3;
	
	printf("Basit Matematik Menusu\n\n");
	printf("1- Karede alan ve cevre hesaplamasi\n");
	printf("2- Girilen sayinin kupu\n");
	printf("3- Dairede alan ve cevre hesaplamasi\n");
	printf("4- 5x^2+7x+9 denkleminin x'e gore sonucu\n");
	printf("5- Dikdortgende alan ve cevre hesaplamasi\n");
	printf("6- Ucgende alan hesaplamasi\n");
	printf("7- Faktoriyel hesaplamasi\n");
	printf("8- Hiz hesaplamasi\n");
	printf("9- Faiz Hesaplamasi\n");
	printf("10- Girilen x Degerine Gore x<=0 ise 2x+7 x>0 ise 4x-15 Islemlerinin Yapilmasi\n");
	printf("11- Kenar sayisi girilen duzgun cokgenin bir ic acisinin ve acilar toplaminin hesaplanmasi\n");
	printf("12- Paralel kenarda alan ve cevre hesaplamasi\n");
	printf("13- Dik silindirin yuzey alan hesaplamalari\n\n");

	printf("Yapmak istediginiz islemi seciniz: ");
	scanf("%d", &secim);
	

	switch(secim)
	{
		case 1:
			system("CLS");
			printf(" Karede Alan ve Cevre Hesaplamasi \n\n");
			int kare_kenar,kare_alan,kare_cevre;
			
			printf("Karenin bir kenar uzunlugunu giriniz: ");
			scanf("%d", &kare_kenar);
			
			kare_alan=kare_kenar*kare_kenar;
			kare_cevre=kare_kenar*4;
			
			printf("Karenin Alani: %d \n", kare_alan);
			printf("Karenin Cevresi: %d", kare_cevre);
			break;
		case 2:
			system("CLS");
			printf(" Girilen Sayinin Kupunu Alma \n\n");
			int sayi,kup;
			
			printf("Kupunu almak istediginiz sayiyi giriniz: ");
			scanf("%d", &sayi);
			
			kup=sayi*sayi*sayi;
			
			printf("Girdiginiz sayinin kupu: %d", kup);
			break;
		case 3:
			system("CLS");
			printf(" Dairede Alan ve Cevre Hesaplamasi \n\n");
			int yaricap,daire_alan,daire_cevre;
			
			printf("Hesaplamak istediginiz yaricapi giriniz: ");
			scanf("%d", &yaricap);
			
			daire_alan=pi*yaricap*yaricap;
			daire_cevre=2*pi*yaricap;
			
			printf("Dairenin alani: %d\n", daire_alan);
			printf("Dairenin cevresi: %d", daire_cevre);
			break;
		case 4:
			system("CLS");
			printf(" 5x^2+7x+9 Denkleminin x'e Gore Sonucu \n\n");
			int x,sayi1;
			
			printf("Hesaplamak istediginiz x degerini giriniz: ");
			scanf("%d", &sayi1);
			
			x=5*(sayi1*sayi1)+(7*sayi1)+9;
			
			printf("Denklemin x'e gore sonucu: %d", x);
			break;
		case 5:
			system("CLS");
			printf(" Dikdortgende Alan ve Cevre Hesaplamasi \n\n");
			int kk,uk,dd_alan,dd_cevre;
			
			printf("Dikdortgene ait kisa kenari giriniz: ");
			scanf("%d", &kk);
			printf("Dikdortgene ait uzun kenari giriniz: ");
			scanf("%d", &uk);
			
			dd_alan=kk*uk;
			dd_cevre=2*(kk+uk);
			
			printf("Dikdortgeninizin alani: %d \n", dd_alan);
			printf("Dikdortgeninizin cevresi: %d", dd_cevre);
			break;
		case 6:
			system("CLS");
			printf(" Ucgende Alan Hesaplamasi \n\n");
			int taban,yukseklik,ucgen_alan;
			
			printf("Ucgeninize ait taban uzunlugunu giriniz: ");
			scanf("%d", &taban);
			printf("Ucgeninize ait yuksekligi giriniz: ");
			scanf("%d", &yukseklik);
			
			ucgen_alan=(taban*yukseklik)/2;
			
			printf("Girmis oldugunuz sayilara ait ucgenin alani: %d", ucgen_alan);
			break;
		case 7:
			system("CLS");
			printf(" Faktoriyel Hesaplamasi \n\n");
			int sayi2;
			int i=1;
			int faktoriyel=1;
			
			printf("Faktoriyelini almak istediginiz sayiyi giriniz: ");
			scanf("%d", &sayi2);
			
			for(i=1;i<=sayi2;i++)
			{
				faktoriyel=i*faktoriyel;
			}
			printf("Faktoriyelin sonucu: %d", faktoriyel);
			break;
		case 8:
			system("CLS");
			printf(" Hiz Hesaplamasi \n\n");
			float hiz=0,zaman,yol;
			
			printf("Yol uzunlugunu giriniz[KM]: ");
			scanf("%f", &yol);
			printf("Gecen zamani giriniz[SAAT]: ");
			scanf("%f", &zaman);
			
			hiz=yol/zaman;
			printf("Hiziniz: %f km/h", hiz);
			break;
			
		case 9:
			system("CLS");
			printf(" Faiz Hesaplamasi \n\n");
			int ana_para,faiz_orani,faiz_yillik,faiz_aylik,faiz_gunluk,faiz_geliri;
			printf("1- Yillik Faiz Hesaplamasi \n");
			printf("2- Aylik Faiz Hesaplamasi \n");
			printf("3- Gunluk Faiz Hesaplamasi \n");
			
			printf("Faiz seciminizi yapiniz [1-3]: ");
			scanf("%d", &secim);
			
			if(secim==1)
			{
				system("CLS");
				printf(" Yillik Faiz Hesaplamasi \n\n");
				
				printf("Ana Paranizi Giriniz: ");
				scanf("%d", &ana_para);
				printf("Faiz Oranini Giriniz: ");
				scanf("%d", &faiz_orani);
				printf("Kalacagi Yil Suresini Giriniz: ");
				scanf("%d", &faiz_yillik);
				
				faiz_geliri=ana_para*faiz_orani*faiz_yillik/100;
				
				printf("Faiz Geliriniz: %d TL\n", faiz_geliri);
				printf("Yeni Ana Paraniz: %d TL", (ana_para+faiz_geliri));
			}
			else if(secim==2)
			{
				system("CLS");
				printf(" Aylik Faiz Hesaplamasi \n\n");
				
				printf("Ana Paranizi Giriniz: ");
				scanf("%d", &ana_para);
				printf("Faiz Oranini Giriniz: ");
				scanf("%d", &faiz_orani);
				printf("Kalacagi Ay Suresini Giriniz: ");
				scanf("%d", &faiz_aylik);
				
				faiz_geliri=ana_para*faiz_orani*faiz_aylik/1200;
				
				printf("Faiz Geliriniz: %d TL\n", faiz_geliri);
				printf("Yeni Ana Paraniz: %d TL", (ana_para+faiz_geliri));	
			}
			else if(secim==3)
			{
				system("CLS");
				printf(" Gunluk Faiz Hesaplamasi \n\n");
				
				printf("Ana Paranizi Giriniz: ");
				scanf("%d", &ana_para);
				printf("Faiz Oranini Giriniz: ");
				scanf("%d", &faiz_orani);
				printf("Kalacagi Gun Suresini Giriniz: ");
				scanf("%d", &faiz_gunluk);
				
				faiz_geliri=ana_para*faiz_orani*faiz_gunluk/36500;
				
				printf("Faiz Geliriiz: %d TL\n", faiz_geliri);
				printf("Yeni Ana Paraniz: %d TL", (ana_para+faiz_geliri));
			}
			else
			{
				printf("Gecersiz Sayi Sectiniz.\n");
				printf("Lutfen Tekrar Deneyiniz!");
			}
			break;
		case 10:
			system("CLS");
			printf(" Girilen x Degerine Gore Farkli Islemlerin Yapilmasi \n\n");
			
			int x1,sonuc;
			
			printf("Hesaplamak Istediginiz x Degerini Giriniz: ");
			scanf("%d", &x1);
			
			if(x1<=0)
			{
				sonuc=(2*x1)+7;
				printf("Girdiginiz x Degerine Gore Sonuc: %d", sonuc);
			}
			else if(x1>0)
			{
				sonuc=(4*x1)-15;
				printf("Girdiginiz x Degerine Gore Sonuc: %d", sonuc);
			}
			else
			{
				printf("Gecersiz x Degeri Girdiniz.\n");
				printf("Lutfen Tekrar Deneyiniz!");
			}
			break;
			
		case 11:
			system("CLS");
			printf(" Kenar Sayisi Girilen Duzgun Cokgenin Bir Ic Acisinin ve Acilar Toplaminin Hesaplanmasi \n\n");
			
			int kenar_sayisi,ic_aci,ic_aci_top;
			printf("Kenar Sayisini Giriniz: ");
			scanf("%d", &kenar_sayisi);
			
			if(kenar_sayisi>=3)
			{
				ic_aci=(kenar_sayisi-2)*180/kenar_sayisi;
				ic_aci_top=(kenar_sayisi-2)*180;
				
				printf("Bir Ic Acisinin Olcusu: %d\n", ic_aci);
				printf("Acilar Toplami: %d", ic_aci_top);
			}
			else
			{
				printf("3'den Az veya Negatif Bir Deger Girdiginiz Icin Hesaplama Yapilamadi.\n");
				printf("Lutfen Tekrar Deneyiniz!");
			}
			break;
			
		case 12:
			system("CLS");
			printf(" Paralel Kenarda Alan ve Cevre Hesaplamasi \n\n");
			
			int taban_uzunluk,kisa_kenar,yukseklik1,pk_alan,pk_cevre;
			
			printf("Paralel Kenarinizin Taban Uzunlugunu Giriniz: ");
			scanf("%d", &taban_uzunluk);
			printf("Paralel Kenarinizin Kisa Kenarini Giriniz: ");
			scanf("%d", &kisa_kenar);
			printf("Paralel Kenarinizin Yuksekligini Giriniz: ");
			scanf("%d", &yukseklik1);
			
			pk_alan=taban_uzunluk*yukseklik1;
			pk_cevre=2*(taban_uzunluk+kisa_kenar);
			
			printf("Paralel Kenarinizin Alani: %d\n", pk_alan);
			printf("Paralel Kenariniz Cevresi: %d", pk_cevre);
			break;
			
		case 13:
			system("CLS");
			printf(" Dik Silindirin Yuzey Alan Hesaplamalari \n\n");
			
			int yaricap1,yukseklik2,yan_yuzey,top_yuzey_alani,bir_taban_alani;
			
			printf("Dik Silindirin Yaricapini Giriniz: ");
			scanf("%d", &yaricap1);
			printf("Dik Silindirin Yuksekligini Giriniz: ");
			scanf("%d", &yukseklik2);
			
			yan_yuzey=2*pi*yaricap1*yukseklik2;
			bir_taban_alani=pi*yaricap1*yaricap1;
			top_yuzey_alani=2*pi*yaricap1*(yaricap1+yukseklik2);
			
			printf("Dik Silindirin Yan Yuzey Alani: %d\n", yan_yuzey);
			printf("Tabanlardan Birinin Alani: %d\n", bir_taban_alani);
			printf("Toplam Yuzey Alani: %d", top_yuzey_alani);
			break;
			
			
		
		default:
			printf("Gecersiz islem girdiniz! Lutfen tekrar deneyiniz.");
		
	
	}
	
	
	return 0;
}
