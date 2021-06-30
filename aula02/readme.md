# Pod

É no Pod que executa os containers

Pode ter mais de um container por Pod, compartilhando IPs,
Mas utilizado só em casos específicos

Se colocar muitos containers em um Pod, na hora de aumentar
o número de container, a aplicação será duplicada

# ReplicaSet

Controla a quantidade de Pods a partir da quantidade informada a ele
Gerencia a escalabilidade e resiliência da aplicação

Negativo: Caso atualize a aplicação, o replicaset não atualiza os pods atuais

# Deployment

Quando atualizar, cria um novo replicaset para gerenciar os novos pods
Mantém o replicaset antigo para fazer uma troca de versão progressiva, e para caso haja um problema com a nova versão, a troca é muito fácil, basta ativar o replicaset antigo e os pods novos são criados

## Rollout

```bash
$ kubectl rollout undo deployment meudployment
```

!["Fluxo deploy"]("https://storage.googleapis.com/cdn.thenewstack.io/media/2017/11/07751442-deployment.png)
