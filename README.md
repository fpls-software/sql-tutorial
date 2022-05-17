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
          <td>id_kasmasuk</td>
          <td>int</td>
          <td>5</td>
          <td>Primary</td>
        </tr>
      </tbody>
    </table>
  <li>
</ol>
