# resumo-do-lab

# ☁️ Azure - Boas Práticas e Resumo de Recursos

Este documento tem como objetivo servir como um guia rápido para usuários que estão começando a trabalhar com o Microsoft Azure, explicando conceitos essenciais como SLA, opções de disponibilidade de máquinas virtuais e contas de armazenamento.

---

## 📊 SLA (Service Level Agreement)

O SLA é o compromisso da Microsoft com a disponibilidade dos seus serviços. Abaixo estão os níveis mais comuns e o tempo máximo de inatividade permitido por semana:

| SLA (%)   | Inatividade Máxima por Semana |
|-----------|-------------------------------|
| 99%       | 1,68 horas                    |
| 99,9%     | 10,1 minutos                  |
| 99,95%    | 5 minutos                     |
| 99,99%    | 1,01 minuto                   |
| 99,999%   | 6 segundos                    |

---

## 🖥️ Opções de Disponibilidade para Máquinas Virtuais no Azure

Ao criar uma máquina virtual, o Azure oferece opções para melhorar a resiliência e garantir maior tempo de atividade. Aqui estão as principais:

### 1. Nenhuma Redundância de Infraestrutura (Padrão)
- **Descrição:** A VM é criada isoladamente, sem tolerância a falhas físicas.
- **Uso indicado:** Testes, desenvolvimento ou serviços não críticos.
- **SLA estimado:** Até 99%.

---

### 2. Conjunto de Disponibilidade (Availability Set)
- **Descrição:** Agrupa duas ou mais VMs para garantir que não fiquem indisponíveis simultaneamente.
- **Benefícios:** Proteção contra falhas de hardware e de atualização.
- **Uso indicado:** Aplicações tradicionais com múltiplas VMs.
- **SLA estimado:** Até 99,95%.

---

### 3. Zona de Disponibilidade (Availability Zone)
- **Descrição:** Distribui as VMs entre diferentes datacenters dentro da mesma região.
- **Benefícios:** Alta tolerância a falhas físicas e regionais.
- **Uso indicado:** Aplicações críticas que não podem ter downtime.
- **SLA estimado:** Até 99,99%.

---

### 4. Conjuntos de Escala de Máquinas Virtuais (VM Scale Sets)
- **Descrição:** Grupo de VMs idênticas que escalam automaticamente com base na demanda.
- **Benefícios:** Autoescalável e tolerância a falhas.
- **Uso indicado:** Cargas variáveis e aplicações modernas.
- **SLA estimado:** Até 99,99% com zonas de disponibilidade.

---

## 📦 Criar Conta de Armazenamento no Azure

Uma **Conta de Armazenamento** no Azure permite armazenar objetos como blobs, arquivos, filas e tabelas.

### Tipos de Conta:
- **Armazenamento V2 (recomendado):** Suporta todos os tipos de dados.
- **Blob Storage:** Otimizado para blobs.
- **General-purpose v1:** Versão anterior, menos recursos.

### Redundância:
- **LRS (Locally-redundant Storage):** Três cópias locais.
- **ZRS (Zone-redundant Storage):** Cópias em zonas distintas da mesma região.
- **GRS (Geo-redundant Storage):** Réplica em outra região para recuperação de desastre.
- **RA-GRS:** Igual ao GRS, com acesso de leitura na réplica.

### Camadas de Acesso:
- **Hot:** Dados acessados com frequência.
- **Cool:** Dados acessados esporadicamente.
- **Archive:** Dados raramente acessados (armazenamento de longo prazo).

---

Se quiser que eu adicione mais seções ou personalize o estilo, só avisar!
