unit uPrincipal;

{$mode objfpc}{$H+}

interface

uses
  Classes, SysUtils, FileUtil, LResources, Forms, Controls, Graphics, Dialogs,
  StdCtrls, uEstante, uLibro;

type

    { TForm1 }

    TForm1 = class(TForm)
        btAdd: TButton;
        btActualizar: TButton;
        eTitulo: TEdit;
        eAutor: TEdit;
        Label1: TLabel;
        Label2: TLabel;
        Label3: TLabel;
        lbMostrar: TListBox;
        procedure btAddClick(Sender: TObject);
        procedure btActualizarClick(Sender: TObject);
        procedure btCargarClick(Sender: TObject);
        procedure btGuardarClick(Sender: TObject);
        procedure FormCreate(Sender: TObject);
    private
    { private declarations }
    public
    { public declarations }
    end;

var
  Form1: TForm1;
  Estante : TEstante;

implementation

{ TForm1 }

procedure TForm1.FormCreate(Sender: TObject);
begin
    Estante := TEstante.Create(TLibro);
end;

procedure TForm1.btAddClick(Sender: TObject);
var
    Libro : TLibro;
begin
    Libro := Estante.Add;
    Libro.Titulo := eTitulo.Text;
    Libro.Autor := eAutor.Text;
    eTitulo.Clear;
    eAutor.Clear;
    ShowMessage('Libro añadido con éxito');
end;

procedure TForm1.btActualizarClick(Sender: TObject);
var
    i : Integer;
begin
    lbMostrar.Clear;
    for i:=0 to Estante.Count - 1 do
    begin
        lbMostrar.Items.Add(Estante.Items[i].Titulo + ' / ' + Estante.Items[i].Autor);
    end;
end;

initialization
  {$I uprincipal.lrs}

end.

