//---------------------------------------------------------------------------

#include <vcl.h>
#pragma hdrstop

#include "Unit1.h"
//---------------------------------------------------------------------------
#pragma package(smart_init)
#pragma link "trayicon"
#pragma resource "*.dfm"
TForm1 *Form1;

//ilosc sekund
int s=0;

//---------------------------------------------------------------------------
__fastcall TForm1::TForm1(TComponent* Owner)
        : TForm(Owner)
{
}
//---------------------------------------------------------------------------

void __fastcall TForm1::Timer1Timer(TObject *Sender)
{
    s++;

    //ZMIENNE ZLICZAJ¥CE ILOSC KOLEJNO GODZIN, MINUT, SEKUND
    int godzin, minut, sekund;
    AnsiString godz, min, sek;

    godzin = s/3600;
    godz = IntToStr(godzin);
    if(godzin<10) godz="0"+godz;

    minut = (s-godzin*3600)/60;
    min = IntToStr(minut);
    if(minut<10) min="0"+min;

    /*for(int i=1; i<=60; i++)
    {
        if (s>=i*3600) min = IntToStr(minut-i*60);
    }*/

    sekund = s-godzin*3600-minut*60;
    sek = IntToStr(sekund);
    if(sekund<10) sek="0"+sek;

    /*for(int i=1; i<=60; i++)
    {
        if (s>=i*60) sek = IntToStr(sekund-i*60);
    }*/



    //if((sekunda>=60)&&(sekunda<(60+10))) sek="0"+sek;
    //if((sekunda>=120)&&(sekunda<(120+10))) sek="0"+sek;


    //if((sekunda>=j*60)&&(sekunda<(j*60+10))) sek="0"+sek;


    Label1->Caption=godz+":"+min+":"+sek;

}
//---------------------------------------------------------------------------

void __fastcall TForm1::TrayIcon1Click(TObject *Sender)
{
    Show();
    Application->BringToFront();
}
//---------------------------------------------------------------------------
