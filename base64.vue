<template>
    <div>
        <script src="./js/base64.js"></script>
        <textarea id="input_text" name="input_text" class="form-control" spellcheck="false" placeholder="请输入"></textarea>
        <textarea id="output_text" name="output_text" class="form-control" spellcheck="false"></textarea>
    </div>

</template>

<script>
function doit() {
  var encoded = Base64["encode" + ($("encodeURI").checked ? "URI" : "")](
    $("srctxt").value
  );
  $("base64").value = encoded;
  $("roundtrip").value = Base64.decode(encoded);
}
export default {};
</script>

