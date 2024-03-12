<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Resposta do Formulário</title>
</head>
<body>
    <main>
        <h2>Resposta do Formulário</h2>
        <p>Aqui estão os dados que você enviou:</p>
        <?php
        // Verifica se os dados foram enviados via método POST
        if ($_SERVER["REQUEST_METHOD"] == "POST") {
            // Obtém os dados do formulário
            $nome = $_POST["campo_nome"];
            $email = $_POST["campo_email"];
            $telefone = $_POST["campo_telefone"];
            $assunto = $_POST["campo_assunto"];
            $mensagem = $_POST["campo_mensagem"];
            $preferencia_contato = $_POST["campo_pref_contato"];
            $onde_encontrou = $_POST["campo_campus"];
            $opcoes = isset($_POST["opcoes"]) ? $_POST["opcoes"] : [];

            // Exibe os dados na página de resposta
            echo "<p><strong>Nome:</strong> $nome</p>";
            echo "<p><strong>Email:</strong> $email</p>";
            echo "<p><strong>Telefone:</strong> $telefone</p>";
            echo "<p><strong>Assunto:</strong> $assunto</p>";
            echo "<p><strong>Mensagem:</strong> $mensagem</p>";
            echo "<p><strong>Preferência de Contato:</strong> $preferencia_contato</p>";
            echo "<p><strong>Campus de Preferência:</strong> $onde_encontrou</p>";
            echo "<p><strong>Opções Adicionais:</strong></p>";
            if (!empty($opcoes)) {
                echo "<ul>";
                foreach ($opcoes as $opcao) {
                    // Tratamento mais legível das opções adicionais
                    switch ($opcao) {
                        case "newsletter":
                            echo "<li>Aceita receber newsletters</li>";
                            break;
                        case "promocoes":
                            echo "<li>Aceita receber promoções por e-mail</li>";
                            break;
                        case "novidades":
                            echo "<li>Aceita receber novidades sobre eventos e cursos</li>";
                            break;
                        case "termos":
                            echo "<li>Aceita os termos e condições</li>";
                            break;
                    }
                }
                echo "</ul>";
            } else {
                // Mensagem mais descritiva quando nenhuma opção é selecionada
                echo "<p>Nenhuma opção adicional foi selecionada.</p>";
            }
        } else {
            echo "<p>Nenhum dado enviado.</p>";
        }
        ?>
    </main>
</body>
</html>
