*&---------------------------------------------------------------------*
*& Report ZTESTE
*&---------------------------------------------------------------------*
*&
*&---------------------------------------------------------------------*
REPORT zteste.

" Interfaces:
"   Define um conjunto de métodos (assinaturas de métodos) que uma classe
"   deve implementar. Esses métodos definem o comportamento que a classe
"   deve ter e como ela deve interagir com outras classes ou objetos

INTERFACE if_exemplo.
  METHODS: imprimir_dados.
ENDINTERFACE.

CLASS cl_exemplo DEFINITION.
  PUBLIC SECTION.
    INTERFACES if_exemplo.
ENDCLASS.

CLASS cl_exemplo IMPLEMENTATION.

  METHOD if_exemplo~imprimir_dados.
    WRITE: /'Olá, mundo!'.
  ENDMETHOD.

ENDCLASS.

START-OF-SELECTION.
  " opção 1
  DATA lo_objl TYPE REF TO if_exemplo.
  lo_objl = NEW cl_exemplo( ).
  lo_objl->imprimir_dados( ).
  " opção 2
  DATA lo_obj2 TYPE REF TO cl_exemplo.
  lo_obj2 = NEW cl_exemplo( ).
  lo_obj2->if_exemplo~imprimir_dados( ).
