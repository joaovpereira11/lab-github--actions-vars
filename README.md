• Por que a Secret aparece no log como ** e a variável aparece normalmente?

Porque a Secret é uma informação sensível (como uma senha ou token), então o GitHub esconde o valor nos logs por segurança. Já a variável comum não é protegida, então aparece normal.

• O Job deploy_app consegue ler a variável BUILD_VERSION criada no Job build_app? Por quê?

Não consegue. Cada job roda separado, como se fosse outra máquina. Então uma variável criada em um job não existe no outro.
