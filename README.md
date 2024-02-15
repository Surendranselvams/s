<?php
if ($_FILES['excelFile']['error'] === UPLOAD_ERR_OK) {
    $tempFilePath = $_FILES['excelFile']['tmp_name'];
    $destinationFilePath = 'uploads/' . $_FILES['excelFile']['name'];
    move_uploaded_file($tempFilePath, $destinationFilePath);
    echo "File uploaded successfully!";
} else {
    echo "Error uploading file.";
}
?>
