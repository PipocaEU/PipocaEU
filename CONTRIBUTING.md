
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
Use id para elementos exclusivos.
Use data-testid para rastreamento de testes automatizados.

Padrões sugeridos para data-testid:

Tipo de Elemento	Prefixo sugerido	Exemplo

```
Botão	btn-	data-testid="btn-login"
Navegação	nav-	data-testid="nav-home"
Input	input-	data-testid="input-email"
Seções específicas	section-	data-testid="section-hero"

```
Boas práticas:


```
Use nomes descritivos em kebab-case.

Não use nomes genéricos (data-testid="button1" ❌).

Evite repetir o mesmo data-testid em múltiplos elementos.

```


✅ Elementos testáveis
Garanta que elementos interativos ou visualmente relevantes (botões, links, inputs, títulos, etc.) possuam data-testid ou id exclusivos.

Exemplo em HTML:
```
<section id="hero" data-testid="section-hero">
  <h2 data-testid="hero-title">Transforme sua carreira</h2>
  <button data-testid="btn-cadastro">Cadastre-se grátis!</button>
  <input type="email" data-testid="input-email" placeholder="Digite seu e-mail" />
</section>
```

📌 Diferença entre id e data-testid:


**id:**

HTML padrão — cada id deve ser único por página.

Usado para navegação ```(<a href="#hero">)```, CSS targeting, ou JavaScript (DOM API).

Pode colidir com estilos ou comportamentos se usado fora do padrão.

Não é ideal para testes automatizados em larga escala, pois pode mudar de propósito ou já estar sendo usado para outro fim.


**data-testid:**

Criado especificamente para testes.

Não interfere no estilo, layout ou comportamento da aplicação.

Mais seguro de usar em testes porque não tem efeito colateral e é totalmente desvinculado da lógica da aplicação.

Permite maior flexibilidade e clareza nos testes automatizados.


✅ Regras gerais
Não repita data-testid no mesmo documento.

