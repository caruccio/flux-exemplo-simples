# Example de como usar o flux para aplicar manifestos em ambientes diferentes

Para gerar os manifestos para os diferentes ambientes, execute:

```
kubectl kustomize homolog/

kubectl kustomize prod/
```

O diretório `base` possui arquivos que compõem o código comum a todos os ambientes.

Nesse exemplo só existe um deployment, mas você pode expandi-lo criando novos arquivos e incluindo-os no `kustomization.yaml`.

Os arquivos `kustomization.yaml` declaram quais arquivos serão bases (campo `resources`) e quais serão usados para sobrepor os valores da base,
conhecidos como `overlays` (campo `patches`).
