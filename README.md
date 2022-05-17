# sql-tutorial
<h1>Tutorial membuat VIEW Laporan KAS </h1>

<strong>Contoh Format Laporan yang diinginkan</strong>
<table border="1">
  <thead style="text-align: center;">
    <th>No</th>
    <th>Kas Masuk</th>
    <th>Kas Keluar</th>
    <th>Saldo</th>
    <th>keterangan</th>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>1000</td>
      <td>0</td>
      <td>1000</td>
      <td>-</td>
    </tr>
     <tr>
      <td>2</td>
      <td>0</td>
      <td>500</td>
      <td>-500</td>
      <td>-</td>
    </tr>
  </tbody>
 </table>
 
<strong>Buat Table Kas Masuk dan Kas Keluar pada Database<strong>
<ol>
  <li>
    Table KAS Keluar dengan nama <code>tb_kaskeluar</code>
    <table border="1">
      <thead style="text-align: center;">
        <th>#</th>
        <th>Coloum Name</th>
        <th>Type Data</th>
        <th>Length</th>
        <th></th>
      </thead>
      <tbody>
        <tr>
          <td>1</td>
          <td>id_kas</td>
          <td>int</td>
          <td>5</td>
          <td>Primary</td>
        </tr>
        <tr>
          <td>3</td>
          <td>kaskeluar</td>
          <td>int</td>
          <td>10</td>
          <td></td>
        </tr>
        <tr>
          <td>4</td>
          <td>keterangan</td>
          <td>varchar</td>
          <td>32</td>
          <td></td>
        </tr>
      </tbody>
    </table>
  </li>
  <li>
    Table KAS Masuk dengan nama <code>tb_kasmasuk</code>
    <table border="1">
      <thead style="text-align: center;">
        <th>#</th>
        <th>Coloum Name</th>
        <th>Type Data</th>
        <th>Length</th>
        <th></th>
      </thead>
      <tbody>
        <tr>
          <td>1</td>
          <td>id_kas</td>
          <td>int</td>
          <td>5</td>
          <td>Primary</td>
        </tr>
        <tr>
          <td>3</td>
          <td>kasmasuk</td>
          <td>int</td>
          <td>10</td>
          <td></td>
        </tr>
        <tr>
          <td>4</td>
          <td>keterangan</td>
          <td>varchar</td>
          <td>32</td>
          <td></td>
        </tr>
      </tbody>
    </table>
  </li>
</ol>

<strong>Query yang dibutuhkan untuk membuat VIEW</strong> <br/>
<code>
  SELECT id_kas, kasmasuk, " " as kaskeluar, (kasmasuk - 0) as saldo FROM tb_kasmasuk <br/>
  </code>
  <code>
  UNION <br/>
  </code>
  <code>
  SELECT id_kas, " " as kasmasuk, kaskeluar, (0 - kaskeluar) as saldo FROM tb_kaskeluar <br/>
  </code>
