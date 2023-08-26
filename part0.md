# 0.4

```mermaid
sequenceDiagram
  participant browser
  participant server
  participant User
  participant JavaScript
  
  User->>browser: write something into the text field (whatever)
  User->>browser: clicking the Save button
  browser->>JavaScript: list = document.getElementsByTagName('ul')[0]
  JavaScript->>server: send the list elements to server
  server->>server: processing
  browser->>JavaScript: newElement = document.createElement('li')
  browser->>JavaScript: newElement.textContent = (whatever)
  JavaScript->>browser: list.appendChild(newElement)
  browser->>User: Exibir Lista Atualizada


