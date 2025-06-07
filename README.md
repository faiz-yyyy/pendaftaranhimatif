<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Form Pendaftaran HIMATIF</title>
  <style>
     body { 
      font-family: Arial, sans-serif; background: linear-gradient(to right, rgb(5, 184, 244), rgb(138, 43, 226));
      padding: 20px; }
    .form-container {
      max-width: 600px; margin: auto; background:rgb(255, 255, 255); padding: 20px;
      border-radius: 8px; box-shadow: 0 0 10px rgb(0, 0, 0);
    } 
    h2 { text-align: center; margin-bottom: 20px; }
    .form-group { margin-bottom: 15px; }
    label { font-weight: bold; display: block; margin-bottom: 5px; }
    input, select, textarea {
      width: 100%; padding: 10px; border-radius: 4px; border: 1px solid #ccc;
    }
    .checkbox-group { display: flex; flex-wrap: wrap; gap: 10px; }
    button {
      background-color:rgb(3, 37, 70); color: white; padding: 10px;
      width: 100%; border: none; border-radius: 5px; font-size: 16px;
    }
  </style>
</head>
<body>

<div class="form-container">
  <h2>Form Pendaftaran Anggota HIMAPRO</h2>
  <form method="POST" enctype="multipart/form-data">

    <div class="form-group">
      <label>Nama Lengkap</label>
      <input type="text" name="nama" required>
    </div>

    <div class="form-group">
      <label>NIM</label>
      <input type="text" name="nim" maxlength="15" required>
    </div>

    <div class="form-group">
      <label>Program Studi</label>
      <select name="prodi" required>
        <option value="">-- Pilih --</option>
        <option>Teknik Informatika</option>
        <option>Sistem Informasi</option>
        <option>Teknologi Informasi</option>
      </select>
    </div>

    <div class="form-group">
      <label>Semester Aktif</label>
      <select name="semester" required>
        <option value="">-- Pilih --</option>
        <option>2</option>
        <option>4</option>
        <option>6</option>
        <option>Lainnya</option>
      </select>
    </div>

    <div class="form-group">
      <label>Tanggal Lahir</label>
      <input type="date" name="tanggal_lahir" required>
    </div>

    <div class="form-group">
      <label>Nomor WhatsApp Aktif</label>
      <input type="tel" name="whatsapp" placeholder="08xxxxxxxxxx" required>
    </div>

    <div class="form-group">
      <label>Email Mahasiswa</label>
      <input type="email" name="email" placeholder="email@student.univ.ac.id" required>
    </div>

    <div class="form-group">
      <label>Unggah KTM (PDF/JPG)</label>
      <input type="file" name="ktm" accept=".pdf,.jpg,.jpeg,.png" required>
    </div>

    <div class="form-group">
      <label>Pilih Divisi yang Diminati</label>
      <div class="checkbox-group">
        <label><input type="checkbox" name="divisi[]" value="Keilmuan"> Keilmuan</label>
        <label><input type="checkbox" name="divisi[]" value="Humas"> Humas</label>
        <label><input type="checkbox" name="divisi[]" value="Kewirausahaan"> Kewirausahaan</label>
        <label><input type="checkbox" name="divisi[]" value="Media dan Informasi"> Media dan Informasi</label>
        <label><input type="checkbox" name="divisi[]" value="Kesekretariatan"> Kesekretariatan</label>
      </div>
    </div>

    <div class="form-group">
      <label>Alasan Bergabung</label>
      <textarea name="alasan" rows="4" required></textarea>
    </div>

    <div class="form-group">
      <label>Unggah File Pendukung Divisi (Opsional)</label>
      <input type="file" name="file_divisi" accept=".pdf,.docx,.jpg,.png">
    </div>

    <button type="submit">Kirim Pendaftaran</button>
  </form>
</div>

</body>
</html>
