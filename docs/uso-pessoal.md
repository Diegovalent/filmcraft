# FilmCraft pessoal — uso e publicação

Distribuição independente de Diegovalent, baseada no FilmCraft da equipe ArtCraft e colaboradores, sob MIT ou Apache-2.0. Os avisos e créditos originais são preservados. Os logotipos ArtCraft restritos foram removidos.

## Ativar a hospedagem (uma vez)

No repositório, abra **Settings → Pages → Build and deployment → Source → GitHub Actions**.
Depois abra **Actions → Publicar FilmCraft Web**. A publicação inicia quando há alterações na branch `main`; também pode ser iniciada em **Run workflow**. O endereço confirmado aparece no job `deploy` quando a publicação termina.

O fluxo compila o código deste repositório. Não baixa executáveis ou versões prontas do repositório original, não sincroniza mudanças externas automaticamente e não depende dos segredos de assinatura do criador. As dependências de código aberto declaradas em Cargo.toml continuam sendo baixadas nas versões do Cargo.lock.

## Usar

Abra o endereço publicado no Chrome ou Edge atualizado. Importe um vídeo local pelo menu de importação, arraste o clipe para a sequência e use Export para baixar o resultado. Teste primeiro com um MP4 curto em H.264/AAC. Salve também o projeto `.fcproj` e mantenha os vídeos originais.

A edição e a renderização acontecem no computador do visitante. O GitHub serve somente os arquivos do aplicativo; este fluxo não adiciona servidor para receber seus vídeos. O navegador pode guardar mídia e recuperação no armazenamento local. Limpar os dados do site pode apagar essas cópias.

## Limites

O FilmCraft ainda está em alfa. A versão web tem menos recursos e pode ser mais lenta que a nativa, sobretudo em vídeos grandes. Projetos Premiere `.prproj` não são suportados. Algumas funções que exigem threads no desktop não funcionam na web. Se houver problema gráfico, teste acrescentar `?webgl` ao endereço.

## Verificação

O fluxo executa as verificações existentes do projeto (`cargo xtask ci`), compila o WebAssembly e confere os arquivos essenciais antes de publicar. Isso não substitui o teste de importação, edição e exportação com seus formatos de vídeo.
