---
title: "Bir sanatçı öner"
slug: suggest-an-artist
---

İsa'yı izleyen müzisyenleri ve sanatçıları duymayı çok seviyorum. Hakkında yazmamı, röportaj yapmamı ya da tepki videosu çekmemi istediğin birini tanıyorsan, burada söyle bana.

Bir isim ve bir bağlantı yeterli — ve neden o, birkaç kelimeyle. Gelen her şeyi okuyorum. Çok teşekkürler.

Tanıdığın biri mi var? Fotoğrafına dokun, form kendiliğinden dolar — sonra neden o olduğunu birkaç kelimeyle ekle ve gönder.

<div class="suggest-carousel" role="list" aria-label="Önerebileceğin müzisyenler ve sanatçılar">
{% for artist in suggest_carousel %}
  <button type="button" class="suggest-pick" role="listitem" data-artist="{{ artist.name }}" data-link="{{ artist.profile }}" title="{{ artist.name }} öner">
    <img src="{{ artist.img }}" alt="{{ artist.name }}" loading="lazy" width="150" height="150">
    <span class="suggest-pick__name">{{ artist.name }}</span>
    <span class="suggest-pick__note">{{ artist.note }}</span>
  </button>
{% endfor %}
</div>

<p class="suggest-carousel__more">Ya da aşağıda yeni birini öner — duymam gerektiğini düşündüğün herkesi.</p>

Bu site 18 yaşından küçükler için değildir.

<form id="suggest-form" class="suggest-form">
  <label for="suggest-artist">Sanatçının adı</label>
  <input id="suggest-artist" name="artist" type="text" maxlength="200" placeholder="Kime bakmalıyım?" required>

  <label for="suggest-link">Sosyal medya profil bağlantısı</label>
  <input id="suggest-link" name="link" type="url" maxlength="500" placeholder="https://www.instagram.com/…" required>

  <fieldset class="suggest-kinds">
    <legend>Onlarla ne yapayım?</legend>
    <label><input type="checkbox" name="kind" value="write"> Hakkında yaz</label>
    <label><input type="checkbox" name="kind" value="interview"> Röportaj yap</label>
    <label><input type="checkbox" name="kind" value="reaction"> Hakkında tepki videosu çek</label>
  </fieldset>

  <label for="suggest-why">Neden o?</label>
  <textarea id="suggest-why" name="why" rows="3" maxlength="500" placeholder="Birkaç kelime yeterli…"></textarea>

  <label for="suggest-name">Adın <span class="optional">(isteğe bağlı)</span></label>
  <input id="suggest-name" name="fromName" type="text" maxlength="100" placeholder="Teşekkür edebileyim diye">

  <label for="suggest-from-link">Sosyal medya profil bağlantın <span class="optional">(isteğe bağlı)</span></label>
  <input id="suggest-from-link" name="fromLink" type="url" maxlength="500" placeholder="https://www.instagram.com/…">

  <button id="suggest-button" type="button">Öneriyi gönder</button>

  <p id="suggest-result" aria-live="polite"></p>
</form>
