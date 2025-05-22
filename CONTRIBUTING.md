
## 🧰 Como contribuir

1. **Fork este repositório**
   - Vá até a página principal do projeto e clique em **Fork**.

2. **Clone o repositório para sua máquina**
   ```bash
   git clone https://github.com/seu-usuario/seu-fork.git

3. **Crie uma branch para sua modificação**

    ```
    git checkout -b minha-contribuicao
    ```

4. **Faça suas alterações** ✨

5. **Commit suas alterações com uma mensagem clara**
    ```
    git commit -m "feat: adicionado componente X"
    ```
    
6. **Envie para o seu fork**
   ```
   git push origin minha-contribuicao
   ```
7. **Abra um Pull Request**

- Vá até a página do seu fork no GitHub e clique em “New Pull Request”.


✅ Boas práticas

🔤 Escrita de código
```
Mantenha a estrutura de pastas e padrões existentes.
Utilize HTML semântico sempre que possível (<section>, <main>, <nav>, etc.).
Agrupe classes do Tailwind por função (layout > espaçamento > cores > tipografia).
Comente trechos de código com propósitos específicos, especialmente se forem complexos ou dinâmicos.
```

## 🧪 Testes 

Para facilitar a criação de testes automatizados, siga estas recomendações:


Para facilitar testes de interface e automação, adote os seguintes padrões:
Adicione identificadores únicos nos elementos-chave da UI:

Use id para elementos e rastreamento de testes automatizados.

Padrões sugeridos para **id**:

```
Botão	btn-	id="btn-login"
Navegação	nav-	id="nav-home"
Input	input-	id="input-email"
Seções específicas	section-	 id="section-hero"

```
Boas práticas:


```
Use nomes descritivos em kebab-case.

Não use nomes genéricos (id="button1" ❌).

Não repita o mesmo id em múltiplos elementos.

```


✅ Elementos testáveis
Garanta que elementos interativos ou visualmente relevantes (botões, links, inputs, títulos, etc.) possuam data-testid ou id exclusivos.

Exemplo em HTML:
```
<section id="hero" data-testid="section-hero">
  <h2 id="hero-title">Transforme sua carreira</h2>
  <button id="btn-cadastro">Cadastre-se grátis!</button>
  <input type="email" id="input-email" placeholder="Digite seu e-mail" />
</section>
```

📌**id:**

HTML padrão — cada id deve ser única.

Criado especificamente para testes.

Não interfere no estilo, layout ou comportamento da aplicação.

Permite maior flexibilidade e clareza nos testes automatizados.


✅ Regras gerais
Não repita data-testid no mesmo documento.

