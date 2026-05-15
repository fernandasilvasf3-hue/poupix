# App de Gerenciamento de Despesas Pessoais

Um aplicativo mobile desenvolvido com React Native para gerenciar despesas pessoais de forma simples e intuitiva.

## 📱 Recursos Principais

- ✅ **Autenticação**: Login e cadastro com Firebase Authentication
- ✅ **Adicionar Despesas**: Interface intuitiva para registrar novas despesas
- ✅ **Listar Despesas**: Visualização de todas as despesas com filtros
- ✅ **Editar/Deletar**: Gerenciar despesas cadastradas
- ✅ **Categorização**: Organizar despesas por 9 categorias diferentes
- ✅ **Relatórios**: Gráficos e estatísticas de gastos
- ✅ **Períodos**: Análise por 1 mês, 3 meses ou 1 ano
- ✅ **Banco de Dados**: Firebase Firestore para sincronização em tempo real

## 🛠️ Tecnologias Utilizadas

- **React Native** 0.72.0
- **Expo** para desenvolvimento rápido
- **Firebase** (Authentication + Firestore)
- **React Navigation** para navegação entre telas
- **Feather Icons** para ícones
- **StyleSheet** para estilização nativa

## 📋 Requisitos do Projeto

### Componentes React Native Implementados:
1. **View** - Estrutura e layout das telas
2. **Text** - Exibição de textos
3. **TextInput** - Campos de entrada de dados
4. **Button/TouchableOpacity** - Elementos interativos
5. **FlatList** - Listas otimizadas
6. **Image** - Exibição de imagens (emojis)
7. **Flexbox Layout** - Sistema de posicionamento
8. **Navegação** - Stack Navigator e Bottom Tab Navigator

### Telas Implementadas (7 telas):
1. **Tela de Login** - Autenticação de usuários
2. **Dashboard** - Resumo e lista de despesas
3. **Adicionar Despesa** - Formulário para nova despesa
4. **Detalhes da Despesa** - Visualizar e editar despesa
5. **Categorias** - Visualizar despesas por categoria
6. **Relatórios** - Gráficos e estatísticas
7. **Configurações** - Preferências e logout

## 🚀 Como Instalar e Usar

### Pré-requisitos
- Node.js (v14 ou superior)
- npm ou yarn
- Expo CLI (`npm install -g expo-cli`)

### Instalação

1. **Clone ou acesse o repositório:**
```bash
cd app-despesas
```

2. **Instale as dependências:**
```bash
npm install
```

3. **Configure o Firebase:**
   - Crie um projeto no [Firebase Console](https://console.firebase.google.com)
   - Obtenha suas credenciais de configuração
   - Atualize `src/services/firebase.js` com suas credenciais:
```javascript
const firebaseConfig = {
  apiKey: "AIzaSyB5pn4Gzv7bwpQ2v_Nwalv3vJXAYEJM1-M",
  authDomain: "poupix-12295.firebaseapp.com",
  projectId: "poupix-12295",
  storageBucket: "poupix-12295.firebasestorage.app",
  messagingSenderId: "54831813958",
  appId: "1:54831813958:web:a02135b262c2e502e74147",
  measurementId: "G-YQTVV8MSH7"
};
```

4. **Inicie a aplicação:**

```bash
# Para web
npm run web

# Para Android
npm run android (#Ta com um pequeno erro pelo Expo Go)


## 📁 Estrutura do Projeto

```
app-despesas/
├── src/
│   ├── screens/
│   │   ├── LoginScreen.js          # Autenticação
│   │   ├── DashboardScreen.js      # Lista de despesas
│   │   ├── AdicionarDespesaScreen.js
│   │   ├── DetailesDespesaScreen.js
│   │   ├── CategoriasScreen.js
│   │   ├── RelatoriosScreen.js
│   │   └── ConfiguracoesScreen.js
│   ├── navigation/
│   │   └── RootNavigator.js        # Configuração de rotas
│   ├── services/
│   │   ├── firebase.js             # Configuração Firebase
│   │   └── despesasService.js      # API de despesas
│   └── styles/
│       ├── colors.js               # Paleta de cores
│       └── styles.js               # Estilos globais
├── App.js                           # Arquivo principal
├── app.json                         # Configuração Expo
├── package.json
└── README.md
```

## 🔐 Funcionalidades de Autenticação

- **Criar Conta**: Novo usuário com email e senha
- **Login**: Acesso com credenciais existentes
- **Logout**: Sair da conta com segurança
- **Persistência**: Dados mantidos localmente com AsyncStorage

## 💰 Gerenciamento de Despesas

### Adicionar Despesa:
- Título obrigatório
- Valor em reais
- Categoria (9 opções com emoji)
- Data (padrão: hoje)
- Descrição opcional

### Visualizar:
- Lista com resumo mensal
- Cada item mostra: título, data, categoria, valor
- Cards com scroll suave

### Editar/Deletar:
- Tap na despesa para detalhes
- Botão editar para modificar
- Confirmação antes de deletar

## 📊 Relatórios e Análises

- **Total de Despesas**: Soma de todas as transações
- **Média de Gastos**: Valor médio por transação
- **Maior Gasto**: Maior transação registrada
- **Menor Gasto**: Menor transação registrada
- **Filtros por Período**: 1 mês, 3 meses, 1 ano

## 🎨 Paleta de Cores

- **Primária**: #6366f1 (Roxo)
- **Secundária**: #ec4899 (Rosa)
- **Sucesso**: #10b981 (Verde)
- **Aviso**: #f59e0b (Amarelo)
- **Perigo**: #ef4444 (Vermelho)

## 📝 Categorias de Despesas

1. 🍔 Alimentação
2. 🚗 Transporte
3. 🏥 Saúde
4. 🎮 Diversão
5. 📚 Educação
6. 💼 Trabalho
7. 🏠 Moradia
8. 💡 Utilidades
9. 📦 Outros

## 🔄 Sincronização com Firebase

- Todos os dados são salvos em Firestore
- Sincronização em tempo real entre dispositivos
- Backup automático na nuvem
- Segurança com regras de Firestore

## 👥 Membros do Projeto

| Membro | Componentes Desenvolvidos |
|--------|--------------------------|
| [Nome 1] | Autenticação, Firebase Config |
| [Nome 2] | Dashboard, Listagem de Despesas |
| [Nome 3] | Adicionar/Editar Despesas |
| [Nome 4] | Categorias, Relatórios |
| [Nome 5] | Configurações, UI/UX |

## 🐛 Troubleshooting

### Erro de Firebase
- Verifique se as credenciais estão corretas
- Confirme se a autenticação está ativada no Firebase Console
- Verifique as regras de segurança do Firestore

### Erro de Navegação
- Limpe o cache: `expo clear`
- Reinstale dependências: `rm -rf node_modules && npm install`

### Problema de Sincronização
- Verifique a conexão com a internet
- Confirme se o usuário está autenticado
- Verifique os logs do Firebase

## 📱 Prints da Aplicação

# Só copiar o link

https://drive.google.com/drive/folders/13jmI9hRI7Z6iCZFKTsHEdHvaH8ABb1fJ?usp=drive_link

## 🚀 Próximas Melhorias

- [ ] Gráficos mais avançados com charts
- [ ] Exportar dados em PDF
- [ ] Modo offline com sincronização posterior
- [ ] Notificações push
- [ ] Compartilhamento de despesas entre usuários
- [ ] Recorrências automáticas
- [ ] OCR para fotografar recibos

## 📄 Licença

MIT License - Livre para uso educacional

## 📞 Suporte

Para dúvidas ou sugestões, entre em contato com a equipe de desenvolvimento.

---

**Desenvolvido para a disciplina de Programação Mobile Coding - 3º Período**
