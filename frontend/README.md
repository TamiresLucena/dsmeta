## Criação backend e frontend

# Checklist

## Ferramentas

- Nodejs 16 e Yarn (vídeo: https://youtu.be/x5tgFTS-CYA )
- STS (vídeo: https://youtu.be/TGQ0K9QsX88 )
- VS Code
  - `IntelliCode`
  - `ESLint`
  - `JSX HTML <tags/>`

## criar projeto ReactJS

```
yarn create vite frontend --template react-ts
```

## Criar projeto Spring Boot

- Criar projeto Spring Boot no `Spring Initializr` com as seguintes dependências:

  - Web
  - JPA
  - H2
  - Security

- Ajuste no arquivo pom.xml:

```xml
<plugin>
	<groupId>org.apache.maven.plugins</groupId>
	<artifactId>maven-resources-plugin</artifactId>
	<version>3.1.0</version><!--$NO-MVN-MAN-VER$ -->
</plugin>
```

- Botão direito no projeto -> Maven -> Update project (force update)

## Datepicker

Documentação: https://github.com/Hacker0x01/react-datepicker

```
yarn add react-datepicker@4.8.0 @types/react-datepicker@4.4.2
```

```javascript
import DatePicker from "react-datepicker";
import "react-datepicker/dist/react-datepicker.css";
```

```javascript
<DatePicker
  selected={new Date()}
  onChange={(date: Date) => {}}
  className="dsmeta-form-control"
  dateFormat="dd/MM/yyyy"
/>
```

## React Hook useState para manter estado das datas

Macete para criar uma data de X dias atrás:

```javascript
const date = new Date(new Date().setDate(new Date().getDate() - 365));
```
