# Ubah tampilan harga woocomerce dari 0 ke tulisan free

<pre>
	function wpgeeks_price_override( $price, $product ) {
	   if ( empty( $product->get_price() ) ) {
	      /*
	       * Replace the word "Free" with whatever text you would like. Also
	       * remember to update the textdomain for translation if required.
	       */
	      $price = __( 'FREE', 'textdomain' );
	   }
	 
	   return $price;
	}
	add_filter( 'woocommerce_get_price_html', 'wpgeeks_price_override', 100, 2 );
</pre>