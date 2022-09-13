<script lang="ts">

import { onMount } from 'svelte';
onMount(() => {
	var tag = document.createElement('script');

tag.src = "https://www.youtube.com/iframe_api";
var firstScriptTag = document.getElementById('player');
firstScriptTag.parentNode.insertBefore(tag, firstScriptTag);

// 3. This function creates an <iframe> (and YouTube player)
//    after the API code downloads.
var player:any;
function onYouTubeIframeAPIReady() {
  player = new YT.Player('player', {
	height: '360',
	width: '640',
	videoId: 'M7lc1UVf-VE',
	events: {
	  'onReady': onPlayerReady,
	  'onStateChange': onPlayerStateChange
	}
  });
}

// 4. The API will call this function when the video player is ready.
function onPlayerReady(event) {
  event.target.playVideo();
}

// 5. The API calls this function when the player's state changes.
//    The function indicates that when playing a video (state=1),
//    the player should play for six seconds and then stop.
var done = false;
function onPlayerStateChange(event) {
  if (event.data == YT.PlayerState.PLAYING && !done) {
	setTimeout(stopVideo, 6000);
	done = true;
  }
}
function stopVideo() {
  player.stopVideo();
}

});
</script>

<div>
	<!-- <audio src="https://www.youtube.com/embed/ftNOCfqoIjQ?controls=0" data-autoplay="0"></audio>
	<iframe width="560" height="315" src="https://www.youtube.com/embed/ftNOCfqoIjQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" ></iframe> 
	<div data-video="ftNOCfqoIjQ" data-autoplay="0" data-loop="1" id="youtube-audio">
	</div>-->
	<div id="player"></div>
	<slot />
</div>

<style>
	div {
		padding: 0;
		margin: 0;
	}
</style>

