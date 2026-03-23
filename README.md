# dio_bc_sec_riachuelo
Bootcamp em segurança da informação promovido pela Dio.me em parceria com a Riachuelo

## Notebook LM Google ##

Criado um notebook LM sobre Dividendos no mundo das ações e FIIs para que tenha informações assertivas sobre esse assunto.
Procurei esse tema pois quero aprofundar meus conhecimentos nessa área, para gerar renda atualmente e futuramente.

Para isso criei uma lista com 23 fontes, sendo 1 de vídeo e 22 de texto, passando por Wikipedia, Bancos, sites de investimento, etc

Eu elaborei um prompt básico que com todas essas informações ele gerasse conteúdo para um blog voltado para o informar/orientar pessoas que desejam entender como isso funciona

Ele me entregou essas saídas, como bullets para um blog e estou gerando um vídeo com essas informações, focado em informar/explicar o que é ganhos com dividendos

## Teste Força Bruta Kali/Medusa ##

Projeto Prático: Testes de Força Bruta com Kali Linux e Medusa

Objetivo

Este projeto tem como finalidade simular ataques de força bruta em serviços vulneráveis utilizando a ferramenta Medusa no Kali Linux, explorando ambientes controlados como Metasploitable 2 e DVWA (Damn Vulnerable Web Application). O intuito é compreender os riscos, documentar os testes e propor medidas de mitigação.

Configuração do Ambiente

Máquinas Virtuais

VM1 - Kali Linux: utilizada como máquina atacante.

VM2 - Metasploitable 2: utilizada como alvo vulnerável.

Rede

Configuração em rede interna (host-only) no VirtualBox.

IPs atribuídos manualmente para facilitar a comunicação:

Kali Linux: 192.168.56.101

Metasploitable 2: 192.168.56.102

Cenários de Ataque

1. Força Bruta em FTP

Serviço alvo: vsftpd no Metasploitable 2.

Wordlist simples criada manualmente (ex.: users.txt e passwords.txt).

Comando utilizado:

medusa -h 192.168.56.102 -u msfadmin -P passwords.txt -M ftp

Validação: acesso obtido ao FTP com credenciais fracas.

2. Automação em Formulário Web (DVWA)

Serviço alvo: login web do DVWA.

Configuração do DVWA em modo low security.

Comando utilizado:

medusa -h 192.168.56.102 -u admin -P passwords.txt -M http -m FORM:/dvwa/login.php:username=^USER^&password=^PASS^:Login Failed

Validação: login realizado com sucesso após tentativa automatizada.

3. Password Spraying em SMB

Serviço alvo: Samba no Metasploitable 2.

Enumeração de usuários realizada previamente.

Comando utilizado:

medusa -h 192.168.56.102 -U users.txt -p 123456 -M smbnt

Validação: acesso obtido com senha fraca compartilhada entre usuários.

Recomendações de Mitigação

Políticas de senha fortes: exigir complexidade mínima e troca periódica.

Bloqueio de tentativas: implementar mecanismos de lockout após falhas consecutivas.

Monitoramento de logs: revisar acessos suspeitos e alertar administradores.

Uso de autenticação multifator (MFA): reduzir impacto de credenciais comprometidas.

Segmentação de rede: limitar exposição de serviços vulneráveis.

Reflexões e Aprendizados

O Medusa demonstrou eficiência em ataques automatizados contra serviços comuns.

Ambientes como Metasploitable 2 e DVWA são ideais para aprendizado seguro.

A prática reforça a importância de defesa em profundidade e da conscientização sobre segurança.

Conclusão

Este projeto prático permitiu compreender como ataques de força bruta podem comprometer sistemas vulneráveis e destacou a necessidade de medidas preventivas robustas. A documentação serve como guia para estudantes e profissionais que desejam explorar segurança ofensiva em ambientes controlados e aplicar boas práticas de defesa em ambientes reais.
