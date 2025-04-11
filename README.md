# 🚀 Sistema de Verificação de Idade para Votação e Alistamento Militar

## 📋 Sobre o Projeto

Sistema web responsa que permite consultar rapidamente as regras de votação e alistamento militar de diversos países com base na idade e sexo do usuário. Quando o usuário seleciona um país, a bandeira da nação é carregada como background da aplicação, dando aquele visual personalizado que deixa todo cliente babando.

## ✨ Funcionalidades

- **Seleção de país** - Interface pra escolher entre vários países cadastrados
- **Verificação de idade** - Validação da idade informada pelo usuário
- **Verificação de sexo** - Tratamento diferenciado baseado no sexo pra regras de alistamento
- **Background dinâmico** - A bandeira do país selecionado é carregada como fundo da página
- **Feedback visual** - Exibição clara se o voto é opcional, obrigatório ou não permitido
- **Responsividade** - Layout que se adapta em diferentes dispositivos (mobile friendly)

## 🛠️ Tecnologias Utilizadas

- **HTML5** - Estruturação semântica da página
- **CSS3** - Estilização com design moderno e responsivo
- **JavaScript (ES6+)** - Manipulação do DOM e regras de negócio
- **SVG** - Renderização das bandeiras com alta qualidade e performance

## 🚀 Como Usar

```bash
# Clone esse repositório 
git clone https://github.com/seu-usuario/verificador-votacao.git

# Acesse a pasta do projeto
cd verificador-votacao

# Abra o arquivo index.html no navegador
# Se tiver Python instalado, pode rodar um servidor rápido:
python -m http.server 8000
```

Ou simplesmente acesse a [demo online](https://seu-usuario.github.io/verificador-votacao) e testa direto na web!

## 🎯 Como Funciona

O sistema opera com base em um objeto JavaScript que mapeia as regras de votação e alistamento militar de cada país. Quando o usuário seleciona um país e informa idade e sexo, a aplicação consulta essas regras e retorna o status correspondente.

```javascript
// Exemplo da estrutura de dados para o Brasil
"BR": {
    name: "Brasil",
    flag: "path/to/brazil-flag.svg",
    voting: {
        optional: [16, 17, 70, 120],  // Opcional para 16-17 e acima de 70
        mandatory: [18, 69],          // Obrigatório entre 18 e 69
        notAllowed: [0, 15]           // Não permitido abaixo de 16
    },
    military: {
        male: {
            mandatory: [18, 45],     // Obrigatório para homens entre 18 e 45
            optional: [17, 17],      // Opcional aos 17
            notRequired: [0, 16, 46, 120]
        },
        female: {
            // Configurações para mulheres
        }
    }
}
```

## 🧑‍💻 Desenvolvido com ❤️ e ☕ [Manoel Gosalan](https://github.com/mgosalan-dev).

Te desejo sucesso nesse projeto, mano! Qualquer bug ou feature, manda aquele PR de lei que vamos analisar.

## 📝 Licença

Este projeto está licenciado sob a licença MIT - veja o arquivo [LICENSE.md](LICENSE.md) para mais detalhes.

## 🔄 Processo de desenvolvimento

Esse projeto começou como um desafio pra testar conhecimentos em JavaScript e evoluiu pra uma aplicação completa de consulta. O processo envolveu:

1. **Levantamento de dados** - Pesquisa das regras de votação em diferentes países
2. **Definição da arquitetura** - Estruturação do objeto de dados e funções
3. **Implementação do frontend** - Desenvolvimento da interface responsiva
4. **Implementação das regras de negócio** - Lógica de verificação das regras
5. **Testes e refinamentos** - Ajustes finais para garantir UX de qualidade.
