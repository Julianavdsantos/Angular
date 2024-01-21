# Angular
Documentação sobre Conceitos Importantes do Angular


# Documentação sobre Conceitos Importantes do Angular

## 2. Componentes

### 2.1 Definição

Componentes são blocos fundamentais no Angular, encapsulando HTML, CSS e lógica JavaScript/TypeScript.

### 2.2 Criando um Componente

```bash
ng generate component NomeDoComponente
```

### 2.3 Estrutura de um Componente

- **Template:** Define a estrutura HTML do componente.
- **Estilos:** Estilos CSS específicos do componente.
- **Classe TypeScript:** Lógica e propriedades associadas ao componente.

## 3. Diretivas

### 3.1 Definição

Diretivas são instruções no HTML que modificam a DOM.

### 3.2 Diretivas Embutidas

- **ngIf:** Controle de exibição condicional.
- **ngFor:** Loop para iteração em listas.

### 3.3 Criando Diretivas Personalizadas

```bash
ng generate directive NomeDaDiretiva
```

## 4. Módulos

### 4.1 Definição

Módulos ajudam a organizar o código em blocos funcionais.

### 4.2 Criando um Módulo

```bash
ng generate module NomeDoModulo
```

### 4.3 Importando Módulos

```typescript
import { OutroModulo } from 'caminho-do-modulo';
```

## 5. Binding de Dados

### 5.1 Unidirecional

```html
{{ expressao }}
```

### 5.2 Bidirecional

```html
[(ngModel)]="propriedade"
```

## 6. Eventos

### 6.1 Sintaxe no HTML

```html
<button (click)="funcao()">
```

### 6.2 Manipulação no TypeScript

```typescript
funcao() {
  // lógica
}
```

## 7. Injeção de Dependência

### 7.1 Definição

Angular possui um sistema de injeção de dependência para facilitar a criação, uso e teste de componentes e serviços.

### 7.2 Exemplo

```typescript
constructor(private meuServico: MeuServico) { }
```

## 8. Serviços

### 8.1 Definição

Serviços são instâncias únicas compartilhadas em toda a aplicação, utilizadas para realizar tarefas comuns.

### 8.2 Criando um Serviço

```bash
ng generate service MeuServico
```

## 9. Roteamento

### 9.1 Configuração de Rotas

```typescript
const rotas: Routes = [
  { path: 'pagina', component: MinhaPaginaComponente }
];
```

### 9.2 Navegação

```html
<a routerLink="/pagina">Ir para Página</a>
```

## 10. HTTP Client

### 10.1 Realizando Solicitações HTTP

```typescript
this.http.get<MeuObjeto>('url-api')
  .subscribe(data => console.log(data));
```

## 11. Observables

### 11.1 Trabalhando com Observables

```typescript
observable.subscribe(
  data => console.log(data),
  erro => console.error(erro),
  () => console.log('Concluído')
);
```

## 12. Testabilidade

### 12.1 Escrevendo Testes Unitários

```typescript
it('deve...', () => {
  // lógica de teste
});
```

## 13. Pipes

### 13.1 Utilizando Pipes

```html
{{ data | date:'dd/MM/yyyy' }}
```

## 14. Guardas de Rotas

### 14.1 Protegendo Rotas

```typescript
canActivate(route: ActivatedRouteSnapshot, state: RouterStateSnapshot): boolean {
  // lógica de autorização
}
```

## 15. Angular CLI

### 15.1 Principais Comandos

- `ng new NomeDoProjeto`: Cria um novo projeto Angular.
- `ng generate component NomeDoComponente`: Gera um novo componente.
- `ng serve`: Inicia o servidor de desenvolvimento.

