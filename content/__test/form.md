---
title: 'Form Test'
template: projects
---

<h1> Registration </h1>

<form name="registration_test" netlify>
<table>
  <tr>
    <td>Full Name </td> <td><input type="text" name="name" /></td>
  </tr>
  
  <tr>
    <td>Email </td> <td><input type="email" name="email" /></td>
  </tr>
  
  <tr>
    <td>Phone </td> <td><input type="tel" name="phone" /></td>
  </tr>

  <tr>
    <td>Applying for </td> 
    <td>
      <input type="radio" name="role" value="talk"> presentation <br>
      <input type="radio" name="role" value="poster"> poster <br>
      <input type="radio" name="role" value="audience"> attendance <br>
    </td>
  </tr>

  <tr>
    <td>Abstract Title </td> <td><input type="text" name="abstract_title" /></td>
  </tr>
  <tr>
    <td>Abstract </td> <td><input type="text" name="abstract_body" /></td>
  </tr>

  <tr> <td> &nbsp; </td>  </tr>
  <tr>
    <td> &nbsp; </td> <td> <button type="submit">Send</button> </td>
  </tr>
</table>
</form>