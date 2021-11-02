#!/bin/python3

import math
import os
import random
import re
import sys

#
# Complete the 'isValid' function below.
#
# The function is expected to return a STRING.
# The function accepts STRING s as parameter.
#


def conta_caracteres(string):
    contador={}
    for letra in string:
        try:
            contador[letra]+=1
        except:
            contador[letra]=1
    return contador


def corrige(string):
    freq_letras = conta_caracteres(string)
    try:
        lista_ordenada = sorted(list(freq_letras.values()))
        menor_chave=min(freq_letras, key=freq_letras.get)
        maior_chave=max(freq_letras, key=freq_letras.get)
        if (lista_ordenada[0] < lista_ordenada[1]):
            if (freq_letras[menor_chave]==1):
                del freq_letras[menor_chave]
                return(freq_letras)
            else:
                freq_letras[menor_chave]=freq_letras[menor_chave]+1
                return(freq_letras)
        elif (lista_ordenada[-1] > lista_ordenada[-2]):
            freq_letras[maior_chave]=freq_letras[maior_chave]-1
            return(freq_letras)
        return freq_letras 
    except:
        return freq_letras
                
def valida_sequencia(freq_letras):
    lista = list(freq_letras.values())
    if (min(lista) == max(lista)):
        return 'YES'
    else:
        return 'NO'

def isValid(string):
    # Write your code here
    freq_letras=corrige(string)
    return valida_sequencia(freq_letras)
     
    
if __name__ == '__main__':
    fptr = open(os.environ['OUTPUT_PATH'], 'w')

    s = input()

    result = isValid(s)

    fptr.write(result + '\n')

    fptr.close()
