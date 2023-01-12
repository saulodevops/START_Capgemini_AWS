** SEGURANÇA NA NUVEM AWS **

>Camadas de segurança a nível de conta: usuário root que controla, que tem acesso a todos os recursos

>IAM
1. Permissões granulares, específicas
2. Acesso mais seguro para aplicações
3. Integração com outros serviços para segurança

>Usuário root
1. Atualização de senha
2. Opção de plano de suporte
3. Permissões de usuários no IAM
4. Alterações na configuração da conta (contato, regiões permitidas, etc.)

A) Recomendações

1. Não utilizar o usuário root para operações do cotidiano
2. Criar usuário no IAM e salvar a chave de acesso do usuário
3. Criar grupo no IAM e atribuir permissões completas de administrador e adicionar o usuário ao grupo
4. Desabilitar e remover a chave do usuário root
5. Login com IAM
6. Armazenar root em algum lugar seguro

B) MFA

1. Habilitar MFA
2. MFA para controle de acesso às APIs

C) Token MFA

1. Google Authentication
2. Authy Authentication (Windows Phone)
3. Dispositivos U2F YUBIKEY
4. MFA de Hardware GEMALTO

D) Utilizar CloudTrail para registros (dedo duro)

1. Rastreamento de atividades de usuário, histórico habilitado por padrão dos últimos 90 dias
2. Para mais de 90 dias, necessário criação de trilha no CloudTrail

E) Habilitar relatório de faturamento no Billing

1. Informações sobre uso dos recursos
2. Entregue no Bucket do S3
3. Monitoramento de cobranças da conta
