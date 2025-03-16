# Scripts Úteis
São alguns scripts que fiz para facilitar alguns procedimentos diários e frequentes.

## Como Tornar um Script Bash Executável e Adicioná-lo ao PATH

Este guia explica como tornar um script Bash executável e adicioná-lo ao `PATH` para que você possa executá-lo de qualquer diretório no terminal. Além disso, destacamos a importância de incluir `#!/bin/bash` no início do arquivo Bash.

---

### Passos para Tornar um Script Bash Executável

####  **Crie o Script Bash**
   - Crie um arquivo com a extensão `.sh` (por exemplo, `meu_script.sh`).
   - No início do arquivo, **sempre inclua** a seguinte linha:
     ```bash
     #!/bin/bash
     ```
     Isso informa ao sistema que o arquivo é um script Bash e deve ser executado usando o interpretador Bash.

   Exemplo de script (`meu_script`):
   ```bash
   #!/bin/bash
   echo "Olá, mundo!"
   ```

### Torna Executável


```bash
chmod +x meu_script
./meu_script
>> Olá, mundo!
```

#### 3. **Adicione os Scripts ao PATH**
   - Para executar os scripts de qualquer diretório:

   1. **Adicione o diretório ao `PATH`**:
      - Edite o arquivo `~/.bashrc`:
        ```bash
        vim ~/.bashrc
        ```
      - Adicione esta linha no final:
        ```bash
        export PATH="$HOME/caminho/Até/A/Pasta/Que/Quiser}:$PATH"
        ```
      - Recarregue o shell:
        ```bash
        source ~/.bashrc
        ```
      - **Feche e Abra o terminal.** 

   2. **Teste o comando em qualquer terminal**:
      ```bash
      meu_script
      ```

---