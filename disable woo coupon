add_action( 'woocommerce_applied_coupon', 'wpm_remove_matched_coupons_for_annuals' );
function wpm_remove_matched_coupons_for_annuals() {
 global $woocommerce;
 
// Set your coupon codes
$momboss=  'momboss';
$momlife = 'momlife';
 
 // Get the cart subtotal in non-decimal number format
 $cart_subtotal = WC()->cart->subtotal;
 
 // If cart subtotal is greatr or equal than 200 remove coupons
		 if ($cart_subtotal >= 200) {
		 if ( $woocommerce->cart->has_discount( $momboss ) || $woocommerce->cart->has_discount( $momlife ) ) {
		 WC()->cart->remove_coupon( $momboss );
		 WC()->cart->remove_coupon( $momlife );
			
			$message ="This Coupon is not allowed for Annual Subscription";
			$message_n ="Coupon code Removed successfully.";

			$notice_type ="error";
			$notice_type_n ="notice";
			wc_add_notice( $message, $notice_type );
			wc_add_notice(  $message_n,  $notice_type_n = 'notice' ); 

			}
		 } 
}
