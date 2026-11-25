## Sistemas Operacionais e Linux

* Fundamentos de Sistemas Operacionais: arquitetura de *kernel*, espaço de usuário (*user space*) e chamadas de sistema (*system calls*)

* Gerenciamento de processos, *threads* e concorrência

* Gerenciamento de memória e paginação

* Estruturas de sistemas de arquivos e controle de I/O

* Fundamentos de administração de ambientes Linux: comandos vitais, gerenciamento de permissões e *shell scripting* (Bash)

* Administração e monitoramento de servidores via interface web (Exemplo: Cockpit)

## Virtualização

* Fundamentos da virtualização: motivação, isolamento de recursos e consolidação de servidores

* Tipos de Hypervisors: Tipo 1 (Bare-metal, ex: Proxmox, Xen, ESXi) e Tipo 2 (Hosted, ex: VirtualBox)

* Abordagens de virtualização: Virtualização completa (Full Virtualization), Paravirtualização e Virtualização em nível de Sistema Operacional (Containers)

* KVM (Kernel-based Virtual Machine): arquitetura base, como transforma o Linux em um hypervisor Tipo 1 e o papel do QEMU

* Paralelo de arquiteturas: Máquinas Virtuais (VMs) tradicionais versus Contêineres (vantagens, desvantagens e casos de uso)

* Ciclo de vida de uma VM: criação, provisionamento, *snapshots*, clonagem e destruição

* Abstração e gestão de hypervisors com Libvirt: arquitetura da API, o *daemon* `libvirtd` e a interface de linha de comando `virsh`

* Armazenamento e Redes Virtuais: formatos de discos virtuais (qcow2, raw) e configuração de interfaces de rede (Bridge, NAT)

## Linguagem de Programação

* Python: sintaxe fundamental, estruturas de controle e manipulação de arquivos

* plpgsql: fundamentos de programação em banco de dados e automação de regras de negócio

## Paradigmas de Programação

* Estruturada: execução sequencial e funções

* Orientada a Objetos (OO): encapsulamento, herança, polimorfismo e abstração

* Funcional: imutabilidade e funções puras

* Multiparadigma: combinação de abordagens para resolução de problemas

* Data-driven programming: separação entre lógica de controle e os dados, ditando o fluxo baseado no estado da informação

## Engenharia e Arquitetura de Software

* Arquitetura de software: fundamentos e desenhos de sistemas escaláveis

* Sistemas multi-tenant:

  * Isolamento físico (instâncias ou bancos separados)

  * Isolamento lógico (compartilhamento de tabelas regulado por `tenant_id`)

* Princípios de Clean Code: nomenclatura, tamanho de funções e minimização de complexidade

* Acrônimos de qualidade: SOLID e KISS

* Design Patterns: padrões de criação, estrutura e comportamento 

## Controle de Versão

* Git e GitHub: operações vitais (commit, push, pull, merge) e navegação de histórico

* Estratégias de ramificação: aprofundamento prático no modelo Git flow

* Arquitetura de código: conceito e gestão de repositórios unificados (Monorepo)

## Qualidade de Código

* Testes unitários: introdução, ciclo de vida do teste, *mocks*/*stubs* e automação (ex: *pytest*, schemathesis )

## Integração e APIs

* Arquitetura de API REST: recursos, URIs (substantivos) e *statelessness*

* Semântica de verbos HTTP: aplicação correta de GET, POST, PUT, PATCH e DELETE

* Códigos de status HTTP: interpretação e uso assertivo (série 2xx, 3xx, 4xx, 5xx)

## Softwares Corporativos

* Produtos de software e arquiteturas: definições e fluxos de dados de sistemas ERP, MRP, CMS e CRM

## Banco de Dados

* PostgreSQL: modelagem relacional, administração básica e consultas

* Monitoramento de Banco: análise de performance, conexões e gargalos de transação

## Computação em Nuvem

* Cloud computing: modelos de serviço (IaaS, PaaS, SaaS) e de implantação (Público, Privado, Híbrido)

* Edge computing: processamento de borda e redução de latência

* Conceitos fundamentais: regiões, zonas de disponibilidade e escalabilidade vertical/horizontal

## Contêineres e Orquestração

* Containers e Docker: anatomia de uma imagem, `Dockerfile`, *registries* e isolamento de rede/volume

* Plataformas como Serviço (PaaS) e orquestradores: abstração do deploy, escalabilidade automática e roteamento (Exemplos: OpenShift, Tsuru)

* Kubernetes, Docker Swarm

## Automação, Deploy e Infraestrutura

* CI/CD (Integração e Entrega Contínuas): conceitos fundamentais de *pipelines* e *builds* automatizados

* Automação de fluxos: construção e gestão de *pipelines* declarativos (Exemplo: GitHub Workflow)

* Infraestrutura como código (IaC): provisionamento declarativo e gestão de estado (Exemplo: Terraform)

* Ambientes do ciclo de vida de software: segregação entre Test, Staging e Production

## Redes e Protocolos

* Modelo OSI e topologia de rede: entendimento das 7 camadas (da física à aplicação)

* Pilha TCP/IP: fundamentos de roteamento e comutação de pacotes

* Protocolos de comunicação (HTTP/HTTPS, SSH, DNS) e mapeamento de portas lógicas

## Segurança da Informação

* Princípios básicos de segurança de computadores e sistemas online: criptografia, certificados SSL/TLS e IAM (Identity and Access Management)

* Mitigação de ameaças e bloqueios: proteção contra ataques de força bruta (Exemplo prático: Fail2ban)

* Pentest e OPSEC: fundamentos de testes de invasão e segurança operacional