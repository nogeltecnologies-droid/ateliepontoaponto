# 🧵 Ateliê Ponto a Ponto - Sistema de Agendamento

Este é um projeto de um sistema web completo para gestão de pedidos de costura e ajustes. O sistema permite que clientes solicitem orçamentos via WhatsApp e oferece um painel administrativo para controle de agenda com bloqueio automático de datas.

## 🚀 Funcionalidades

### 📱 Área do Cliente (`index.html`)
* **Formulário Inteligente:** Captura dados do cliente, tipo de peça e serviço necessário.
* **Calendário Dinâmico:** Utiliza *Flatpickr* para exibição de datas.
* **Bloqueio de Datas:** Dias marcados como ocupados no banco de dados ficam indisponíveis para novos clientes.
* **Integração WhatsApp:** Envia o resumo do pedido diretamente para o celular da costureira.

### 🔐 Painel Administrativo (`admin.html`)
* **Acesso Restrito:** Proteção por código de confirmação.
* **Dashboard:** Visão geral de pedidos pendentes e datas bloqueadas.
* **Gestão em Tempo Real:** Aprovação ou exclusão de pedidos com atualização instantânea via Firebase.
* **Agenda & Bloqueios:** Permite bloquear datas manualmente (feriados, folgas) ou automaticamente ao aprovar um pedido.

## 🛠️ Tecnologias Utilizadas

* **HTML5 / CSS3 / JavaScript**
* **Tailwind CSS:** Para um design moderno e responsivo.
* **Firebase Firestore:** Banco de dados NoSQL em tempo real.
* **FontAwesome:** Ícones do sistema.
* **Flatpickr:** Biblioteca de seleção de datas.

## ⚙️ Como Configurar

1.  **Firebase:**
    * Crie um projeto no [Firebase Console](https://console.firebase.google.com/).
    * Ative o **Firestore Database**.
    * Nas **Regras**, utilize:
        ```javascript
        allow read, write: if true;
        ```
    * Crie as coleções `pedidos` e `bloqueios`.

2.  **Hospedagem no GitHub:**
    * Suba os arquivos `index.html` e `admin.html` para o seu repositório.
    * Ative o **GitHub Pages** nas configurações do repositório.

3.  **Acesso Admin:**
    * Acesse `seusite.com/admin.html`.
    * O código de acesso padrão configurado é: `PONTOA`.

## 📂 Estrutura de Arquivos

```text
├── index.html          # Página principal (Cliente)
├── admin.html          # Painel de controle (Administrador)
└── README.md           # Documentação do projeto
