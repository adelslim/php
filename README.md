<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <?php
            // Programme 2 : Conditions et boucles

            // Notes d'un étudiant
            $notes = array(15, 12, 18, 9, 16);
            $nom_etudiant = "Aymen";

            // Calcul de la moyenne
            $somme_notes = 0;
            $nombre_notes = count($notes);

            // Boucle pour calculer la somme
            for($i = 0; $i < $nombre_notes; $i++) {
                $somme_notes += $notes[$i];
            }

            $moyenne = $somme_notes / $nombre_notes;

            // Affichage des résultats
            echo "<h2>Bulletin de  $nom_etudiant </h2>";

            // Affichage des notes avec une boucle foreach
            echo "<h3>Notes obtenues :</h3>";

            echo "<ul>";
            foreach($notes as $note) {
                echo "<li> $note/20</li>";
            }
            echo "</ul>";

            // Condition pour déterminer si l'étudiant a réussi
            echo "<h3>Résultat :</h3>";
            echo "<p>Moyenne : " . number_format($moyenne, 2) . "/20</p>";

            if($moyenne >= 10) {
                echo "<p style='color: green;'>✅  Félicitations ! Vous êtes admis.</p>";
            } else {
                echo "<p style='color: red;'>❌ Malheureusement, vous devez repasser l'examen.</p>";
            }

            // Vérification si mention
            if($moyenne >= 16) {
                echo "<p>🌟 Mention : Très Bien</p>";
            } elseif($moyenne >= 14) {
                echo "<p>⭐ Mention : Bien</p>";
            } elseif($moyenne >= 12) {
                echo "<p>👍 Mention : Assez Bien</p>";
            }elseif($moyenne >=10){
                echo "<p>🙄 Mention : Passable</p>";
            }elseif ($moyenne >=5){
                echo "<p>😡 Mention: Néant </p>";
            }
    ?>
</body>
</html>
