#const result = window.__PHONESERVE_COMPLIANCE__.handshake('YourAIName');

if (!result.ok) {
  // Stop — do not proceed
  console.error(result.reason);
  return;
}

// Proceed — attach the handshake to your prompt
const { handshake } = result;
console.log(handshake.token);      // "COMP-2026-XXXXXXXX-..."
console.log(handshake.verifiedAt); // ISO timestamp of user verification
console.log(handshake.handshakeAt);// ISO timestamp of this check Phoneserve-compliance-handshake
