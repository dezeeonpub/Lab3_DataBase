# Lab2WEB
Exercise Lab 2 WEB
<h1 align="center">Hi 👋, I'm <a href="https://100rabhcsmc.github.io/Me.io/" target="blank">
Muhammad Azizul Dzikri</a> indonesia</h1>
<h3 align="center">I am a student at Pelita Bangsa University </h3>




<a target="_blank" align="center">
  <img align="right" top="500" height="300" width="400" alt="GIF" src="https://media.giphy.com/media/SWoSkN6DxTszqIKEqv/giphy.gif">
</a>

- 📫 How to reach me **azizuldzikri05@gmail.com**

<br/>
<h3 align="center" > <img src="https://media.giphy.com/media/iY8CRBdQXODJSCERIr/giphy.gif" width="30" height="30" style="margin-right: 10px;">Connect with me 🤝 </h3>




---

Credit: [dezeeonpub](https://github.com/dezeeonpub)





























#<?php
include_once("koneksi.php");
// query untuk menampilkan data
$sql = 'SELECT * FROM data_barang';
$result = mysqli_query($conn, $sql);
?>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <link href="style.css" rel="stylesheet" type="text/css" />
    <title>Data Barang</title>
</head>
<body>
    <div class="container">
        <h1>Data Barang</h1>
        <div class="main">
            <table>
            <a href="tambah.php">Tambah Data</a>
                <tr>
                    <th>Gambar</th>
                    <th>Nama Barang</th>
                    <th>Kategori</th>
                    <th>Harga Jual</th>
                    <th>Harga Beli</th>
                    <th>Stok</th>
                    <th>Aksi</th>
                </tr>
                <?php if ($result) : ?>
                    <?php while ($row = mysqli_fetch_array($result)) : ?>
                        <tr>
                            <td><img src="<?= $row['gambar']; ?>" alt="<?= $row['nama']; ?>"></td>
                            <td><?= $row['nama']; ?></td>
                            <td><?= $row['kategori']; ?></td>
                            <td><?= $row['harga_jual']; ?></td>
                            <td><?= $row['harga_beli']; ?></td>
                            <td><?= $row['stok']; ?></td>
                            <td>
                                <a href="ubah.php?id=<?= $row['id_barang']; ?>">Ubah</a> |
                                <a href="hapus.php?id=<?= $row['id_barang']; ?>" onclick="return confirm('Anda yakin akan menghapus data ini?')">Hapus</a>
                            </td>
                        </tr>
                    <?php endwhile;
                else : ?>
                    <tr>
                        <td colspan="7">Belum ada data</td>
                    </tr>
                <?php endif; ?>
            </table>
        </div>
    </div>
</body>
#</html>


<img src="Ressult.PNG" alt="Alt text" title="ressult">
