# odevevevev.c

//dizinin ortalama degerinden daha kucuk ve daha buyuk olan degeri donduren fonks

#include<stdio.h>

float ortalama(int dizi[]);
int ortdanBuyuk(int dizi[]);
int ortdanKucuk(int dizi[]);

int main()
{
	int sayilar[5];
	int dizi[5];
	
	for(int i=0;i<5;i++)
	{
		printf("%d. sayiyi giriniz." , i+1);
		scanf("%d" , &sayilar[i]);
	}
	
	printf("ortalama: %d\n" , ortalama(dizi));
	printf("ortalamadan buyuk olan deger: %d\n" , ortdanBuyuk(sayilar));
	printf("ortalamadan kucuk olan deger: %d\n" , ortdanKucuk(sayilar));
	return 0;
}

float ortalama(int dizi[5])
{
	int toplam;
	
	for(int i=0;i<5;i++)
	{
	toplam+=dizi[i];	
	}
	
	float ort=toplam/5;
	
	return ort;
}

int ortdanBuyuk(int dizi[])
{
	int odb,ort;
	odb=0;
	
	for(int i=0;i<5;i++)
	{
		if(odb<ort)
		{
			odb=ort;
		}
	}
	return odb;	
}

int ortdanKucuk(int dizi[])
{
	
	int odk,ort;
	odk=0;
	
	for(int i=0;i<5;i++)
	{
		if(odk>ort)
		{
			odk=ort;
		}
	}
	return odk;
}
