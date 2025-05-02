# Personaliza-o-do-Prompt-do-CMD
Este guia mostra como personalizar o prompt do CMD no Windows, usando UTF-8, símbolos especiais e cores ANSI
# custom_cmd
Personalização do Prompt do CMD 

# Personalização do Prompt do CMD com UTF-8 e Cores

Este guia mostra como personalizar o prompt do CMD no Windows, usando **UTF-8**, **símbolos especiais** e **cores ANSI**.

---

## 🛠️ Instruções para ativar o prompt estilizado

1. **Criar o arquivo de inicialização `custom.cmd`:**

```cmd
@echo off
chcp 65001 >nul
prompt $E[1;35;40m› $E[1;32;40m⟨$p⟩$E[1;33;40m 
cd /d C:\Seu\Diretorio\Desejado
```

2. **Registrar no Registro para inicializar com o CMD:**

Salve como `custom.reg`:

```reg
Windows Registry Editor Version 5.00

[HKEY_CURRENT_USER\Software\Microsoft\Command Processor]
"AutoRun"="C:\CAMINHO\PARA\custom.cmd"
```

---

## 🎨 Códigos de Cores ANSI para Prompt

| Código | Cor do Texto  | Fundo |
|--------|---------------|-------|
| 30     | Preto         | 40    |
| 31     | Vermelho      | 41    |
| 32     | Verde         | 42    |
| 33     | Amarelo       | 43    |
| 34     | Azul          | 44    |
| 35     | Magenta       | 45    |
| 36     | Ciano         | 46    |
| 37     | Branco/Cinza  | 47    |

Formato: `$E[<estilo>;<cor texto>;<cor fundo>m`

Exemplo: `$E[1;32;40m` (Verde com fundo preto)

---

## ⬅️ Alternativas Estilizadas para `<` e `>`

| Símbolo | Nome                       | Unicode  | Descrição                    |
|---------|----------------------------|----------|------------------------------|
| ‹       | Menor que simples          | U+2039   | Pequeno e elegante           |
| ›       | Maior que simples          | U+203A   | Pequeno e elegante           |
| «       | Aspas angulares esquerdas | U+00AB   | Dois "menor que" juntos      |
| »       | Aspas angulares direitas  | U+00BB   | Dois "maior que" juntos      |
| ⟨       | Colchete angular esquerdo | U+27E8   | Curvado, estilo tribal        |
| ⟩       | Colchete angular direito  | U+27E9   | Curvado, estilo tribal        |
| ⧼       | Colchete decorativo       | U+29FC   | Mais detalhado               |
| ⧽       | Par do acima              | U+29FD   | Par com o anterior           |

---

## 🌙 Temática Lobo / Noite / Tribal – Símbolos Recomendados

| Símbolo | Significado sugerido       | Unicode  |
|---------|----------------------------|----------|
| ☾       | Lua crescente               | U+263E   |
| ☽       | Lua minguante               | U+263D   |
| ✦       | Estrela pontiaguda         | U+2726   |
| ✧       | Estrela de 4 pontas        | U+2727   |
| ⚔       | Espadas cruzadas           | U+2694   |
| ☠       | Caveira                    | U+2620   |
| ⛧       | Pentagrama invertido       | U+26E7   |
| Δ       | Delta (montanha)           | U+2206   |
| Λ       | Lambda (forma de lobo)     | U+039B   |
| Ø       | Tribal, vazio              | U+00D8   |
| Ψ       | Psi (mente, espírito)      | U+03A8   |
| ⚡       | Raio                      | U+26A1   |
| ☄	  | Cometa					   | U+2604	  |
| 🐺	  | Lobo					   | U+1F43A  |

---

## 💡 Exemplo final estilizado:

```cmd
prompt $E[1;32;40m→ $E[0;36;40m$p$E[1;32;40m → $E[1;31;40m🐺 ‹Kildery›$E[1;32;40m → $E[0;32;40m 
```

---

