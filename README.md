# rededecomp-sistemas
Analisador de Rede - Verificador de Conectividade IP.  Ferramenta web para análise de redes IP, conversão de máscaras e verificação de segmentos de rede.
[README.txt](https://github.com/user-attachments/files/22608363/README.txt)
README - VERIFICADOR DE REDE
=============================

DESCRIÇÃO DO PROJETO:
Software que verifica se dois IPs estão na mesma rede, baseado em uma máscara de rede.

FUNCIONALIDADES IMPLEMENTADAS:
1. IP fixo de origem: 192.168.1.10
2. Recebe máscara de rede em bits (ex: 24)
3. Recebe IP de destino do usuário
4. Converte máscara para formato decimal
5. Verifica se IPs estão na mesma rede
6. Interface web intuitiva

PASSO A PASSO DO DESENVOLVIMENTO:
---------------------------------

FASE 1: ESTRUTURA BÁSICA
1. Criamos o arquivo HTML com interface visual
2. Definimos o IP fixo: 192.168.1.10
3. Criamos campos para entrada de dados:
   - Mascara em bits (0-32)
   - IP de destino
4. Implementamos design responsivo e profissional

FASE 2: CONVERSÃO DE MÁSCARA
1. Função mascaraBitsParaDecimal():
   - Converte bits (ex: 24) para decimal (ex: 255.255.255.0)
   - Cria sequência binária de 1's e 0's
   - Divide em 4 octetos
   - Converte cada octeto para decimal

FASE 3: VERIFICAÇÃO DE REDE
1. Função ipParaBinario():
   - Converte IP para formato binário (32 bits)
2. Função aplicarMascara():
   - Aplica máscara nos IPs (AND lógico)
   - Extrai parte da rede
3. Função verificarRede():
   - Compara redes de origem e destino
   - Mostra resultado visual (✅/❌)

COMO USAR:
----------
1. Abra o arquivo 'verificador-rede.html' no navegador
2. O IP fixo já está definido (192.168.1.10)
3. Digite a máscara em bits (ex: 24, 16, 28)
4. Digite o IP de destino (ex: 192.168.1.20)
5. Clique em "Verificar Rede"
6. Veja os resultados:
   - Máscara em formato decimal
   - Se está ou não na mesma rede

EXEMPLOS DE TESTE:
------------------
✅ MESMA REDE:
   Mascara: 24 | IP Destino: 192.168.1.50
   Resultado: "ESTÁ na mesma rede"

❌ REDES DIFERENTES:
   Mascara: 24 | IP Destino: 192.168.2.10
   Resultado: "NÃO ESTÁ na mesma rede"

✅ MESMA REDE (mascara diferente):
   Mascara: 16 | IP Destino: 192.168.5.100
   Resultado: "ESTÁ na mesma rede"

TECNOLOGIAS UTILIZADAS:
-----------------------
- HTML5
- CSS3 (estilização)
- JavaScript (lógica)

-----------------

PARA APRESENTAÇÃO:
-----------------
1. Explique que dois IPs estão na mesma rede quando a parte da rede (definida pela máscara) é igual
2. Demonstre com exemplos práticos
3. Mostre a conversão binária por trás dos cálculos
4. Todos do grupo devem entender a lógica do AND com a máscara

ARQUIVOS:
--------
- verificador-rede.html (versão final completa)

Desenvolvido com sucesso.
