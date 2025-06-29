### 1. Quais os dois tipos de serviços de transporte que a internet prove as suas aplicações? Cite características.

TCP e UDP. Enquanto o TCP é orientado à conexão, mantendo-a durante toda a comunicação, o UCP envia os dados diretamente sem a necessidade de estabelecer uma conexão.

TCP:
- inclui mecanismos de controle de fluxo para evitar com que a rede sobrecarregue haja perda de dados (mais confiável) 
- consome mais recursos de rede e do sistema devido os mecanismos de controle e confiabilidade (mais pesado)
- utilizado na navegação web (HTTP/HTTPS), transferência de arquivos (FTP) e serviços de e-mail (SMTP, IMAP, POP3)

UDP:
- não garente a entrega dos pacotes de dados pois não há mecanismo de retransmissão de pacotes perdidos. (menos confiável)
- mais simples e consome menos recursos, ideal para aplicações que requerem baixa latência como serviços de streaming ou jogos online (mais leve)
- utilizado em serviços de streaming de áudio e vídeo (VoIP, IPTV), consultas DNS regulares e broadcasts 

---

### 2. Suponha que exista exatamente 1 comutador de pacotes entre um computador de origem e um de destino. As taxas de transmissão entre o comutador e a origem e o comutador são os seguintes valores:
dproc = 3 ms \
dqueue = 1,5 ms \
dtrans = 5 ms \
dprop = 3 seg \
- Qual a taxa final?
- Que tipo de equipamento está sendo usado entre os dispositivos?

dnó = dproc + dqueue + dtrans + dprop
dnó = 2*(3ms) + 2*(1.5ms) + 2*(5ms) + 3s
dnó = 6ms + 3ms + 10ms + 3s
dnó = 19ms + 3s

A taxa final será de 3s e 19ms.
O equipamento é o switch, utilizado em curtas distâncias. 

---

### 3. Caravana de dez carros
- Os carros se “propagam” a 100
km/h
- O pedágio leva 12 seg para atender
um carro (tempo de transmissão)
- carro ~ bit
- caravana ~ pacote
- Distância entre 2 pedágios = 200 km

a) Quanto tempo TOTAL leva até que a caravana esteja enfileirada antes do terceiro pedágio?

dprop = 2h
dqueue = 120s (12s x 10 carros)
2*(2h) + 2*(120s)

A caravana de dez carros demora 4h e 4min para enfileirar-se antes do terceiro pedágio.

b) Repita considerando que haja 7 carros no comboio

dprop = 2h
dqueue = 84s
2*(2h) + 2*(84s)

A caravana de sete carros demora 4h, 2min e 48s para enfileirar-se antes do terceiro pedágio.
