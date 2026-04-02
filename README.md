# Meu Projeto CI

## Validação Parte 3

Saída do comando `act -l` (considerando o pipeline principal):

Stage 0:
  setup-e-lint

Stage 1:
  testes-unitarios
  scan-de-seguranca

Stage 2:
  build-e-deploy

  ## Validação Parte 4

É possível comprovar que o Job 2 (testes-unitarios) e o Job 3 (scan-de-seguranca) rodaram em paralelo observando a saída do terminal durante a execução com o act.

Após a conclusão do Job 1 (setup-e-lint), ambos os jobs iniciam ao mesmo tempo, pois possuem dependência apenas do primeiro job.

Durante a execução, os logs aparecem de forma intercalada no terminal, indicando que os dois jobs estão sendo executados simultaneamente.

Além disso, cada job é executado em um contêiner Docker separado, o que reforça que a execução ocorre em paralelo e de forma independente.
