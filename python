# Importando bibliotecas
import pandas as pd
import matplotlib.pyplot as plt

# 1. Criando dados de exemplo (simulando coleta via formulário)
dados = {
    "Nome": ["Alice", "Bruno", "Carla", "Daniel", "Eva"],
    "Horas_Estudo_Semana": [5, 12, 8, 3, 10],
    "Notas_Prova": [7.5, 9.0, 8.0, 6.0, 8.5]
}

df = pd.DataFrame(dados)

# 2. Publicando a tabela em CSV
df.to_csv("analise_dados.csv", index=False)
print("Tabela CSV gerada:\n")
print(df)

# 3. Estatísticas descritivas
print("\nEstatísticas descritivas:")
print(df.describe())

# 4. Comparando notas com referência externa (ex: média da turma é 7.8)
media_referencia = 7.8
df["Acima_Media"] = df["Notas_Prova"] > media_referencia
print("\nComparação com média de referência (7.8):")
print(df[["Nome", "Notas_Prova", "Acima_Media"]])

# 5. Gerando gráficos
plt.figure(figsize=(8,5))
plt.bar(df["Nome"], df["Horas_Estudo_Semana"], color='skyblue')
plt.axhline(y=media_referencia, color='red', linestyle='--', label="Média referência")
plt.title("Horas de estudo por aluno vs média de referência")
plt.xlabel("Alunos")
plt.ylabel("Horas de estudo")
plt.legend()
plt.show()
