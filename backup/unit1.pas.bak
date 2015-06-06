unit Unit1;

{$mode objfpc}{$H+}

interface

uses
  Classes, SysUtils, FileUtil, Forms, Controls, Graphics, Dialogs, DBGrids,
  StdCtrls, ZConnection, ZDataset, db;

type

  { TForm1 }

  TForm1 = class(TForm)
    Button1: TButton;
    Button2: TButton;
    Button3: TButton;
    Button4: TButton;
    Datasource1: TDatasource;
    DBGrid1: TDBGrid;
    Kelas: TEdit;
    Email: TEdit;
    Label1: TLabel;
    Label2: TLabel;
    Label3: TLabel;
    Label4: TLabel;
    NIS: TEdit;
    Nama: TEdit;
    ZConnection1: TZConnection;
    ZQuery1: TZQuery;
    ZQuery2: TZQuery;
    procedure Button1Click(Sender: TObject);
    procedure Button2Click(Sender: TObject);
    procedure Button3Click(Sender: TObject);
    procedure Button4Click(Sender: TObject);
  private
    { private declarations }
  public
    { public declarations }
  end;

var
  Form1: TForm1;

implementation

{$R *.lfm}

{ TForm1 }

procedure TForm1.Button1Click(Sender: TObject);
begin
  ZQuery2.SQL.Clear;
  try
    ZQuery2.SQL.add('insert into siswafour values("'+NIS.text+'","'+Nama.text+'","'+Kelas.text+'","'+Email.text+'")');
    ZQuery2.ExecSQL;
    Showmessage('Succes......!!!!');
  except
    Showmessage('Duh...Gagal...Caba Lagi Yo...');
  end;
   ZQuery1.refresh;
end;

procedure TForm1.Button2Click(Sender: TObject);
begin
    ZQuery2.SQL.Clear;
  try
    ZQuery2.SQL.add('update siswafour set NIS="'+NIS.text+'",Nama="'+Nama.text+'",Kelas="'+Kelas.text+'",Email="'+Email.text+'" Where NIS="'+NIS.text+'"');
    ZQuery2.ExecSQL;
    Showmessage('Succes......!!!!');
  except
    Showmessage('Duh...Gagal...Caba Lagi Yo...');
  end;
   ZQuery1.refresh;
end;

procedure TForm1.Button3Click(Sender: TObject);
var
 Userstring: string;
begin
  if inputquery('Hapus Mas','Masukkan NIS yang akan dihapus', Userstring)
  then
      Begin
      ZQuery2.SQL.Clear;
      try
         ZQuery2.SQL.add('delete from siswafour where NIS="'+userstring+'"');
         ZQuery2.ExecSQL;
         Showmessage('Succes......!!!!');
      except
      Showmessage('Duh...Gagal...Caba Lagi Yo...');
      end;
          ZQuery1.refresh;
      end
  else begin end
end;

procedure TForm1.Button4Click(Sender: TObject);
begin
   Application.terminate;
end;

end.

