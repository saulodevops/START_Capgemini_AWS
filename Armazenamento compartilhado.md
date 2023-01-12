** ARMAZENAMENTO COMPARTILHADO **

Várias instâncias, quando precisam utilizar o mesmo armazenamento: EFS ou FSX

>EFS
a) Sistema de arquivos para compartilhamento entre recursos da aws (instâncias EC2 conseguem enxergar o mesmo disco)
b) Serve para workloads e aplicações
c) Diretórios iniciais, testes em aplicações, backups de bancos de dados, análise de dados BIGDATA, sistemas de arquivos para empresas e fluxos de trabalho de mídia
d) Linux

>FSX for Windows
a) Sistema de arquivos para compartilhamento entre recursos no Windows server
b) NTFS
c) Namespaces DFS e replicação
d) Compatível com SSD de alta performance
e) Diretórios iniciais, lift and shift, fluxo de mídia, análise de dados, desenvolvimento de software

>FSX for Lustre
a) Sistema de arquivos para Lustre
b) Alta performance