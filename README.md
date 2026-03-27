# musical-parakeetimport base64

def try_decode(s):
    try:
        return base64.b64decode(s).decode('utf-8')
    except:
        return None

input_str = "o1hn8h6a7t1l7z7zq3om2t1e7i7f8v6gx5wg1t6s3u8z6l9fr1vj9c8n6u8i7p7dn4hs2e2w8k3m1l4hu3ys9b5t1y1z4q8jm5lk7l9u8z2s2g7b"

# Try filtering digits
filtered_chars = "".join([c for c in input_str if not c.isdigit()])
print(f"Chars only: {filtered_chars}")

# Try filtering letters
filtered_digits = "".join([c for c in input_str if c.isdigit()])
print(f"Digits only: {filtered_digits}")

# Check length
print(f"Length: {len(input_str)}")
"Asm.fif" include
PROGRAM{
  -1 DECLMETHOD recv_external
  DECLPROC recv_internal
  76407 DECLMETHOD is_plugin_installed
  78748 DECLMETHOD get_public_key
  81467 DECLMETHOD get_subwallet_id
  85143 DECLMETHOD seqno
  107653 DECLMETHOD get_plugin_list
  recv_external PROC:<{
    9 PUSHPOW2
    LDSLICEX
    DUP
    32 LDU
    32 LDU
    32 LDU
    s0 s2 XCHG
    NOW
    LEQ
    36 THROWIF
    PUSHROOT
    CTOS
    32 LDU
    32 LDU
    256 LDU
    LDDICT
    ENDS
    s4 s3 XCPU
    EQUAL
    33 THROWIFNOT
    s5 s1 XCPU
    EQUAL
    34 THROWIFNOT
    s0 s5 XCHG
    HASHSU
    s0 s6 s4 XC2PU
    CHKSIGNU
    35 THROWIFNOT
    ACCEPT
    s4 PUSH
    INC
    NEWC
    32 STU
    s4 s(-1) PUXC
    32 STU
    s3 s(-1) PUXC
    256 STU
    s1 s(-1) PUXC
    STDICT
    ENDC
    POPROOT
    COMMIT
    SWAP
    8 LDU
    OVER
    ISZERO
    <{
      5 1 BLKDROP2
      <{
        DUP
        SREFS
      }> PUSHCONT
      <{
        8 LDU
        LDREF
        s0 s2 XCHG
        SENDRAWMSG
      }> PUSHCONT
      WHILE
      DROP
    }> PUSHCONT
    IFJMP
    OVER
    1 EQINT
    <{
      8 LDI
      LDGRAMS
      LDREF
      LDREF
      s2 PUSH
      HASHCU
      s0 s5 XCHG
      NEWC
      8 STI
      s1 s5 XCHG
      256 STU
      ENDC
      CTOS
      7 PUSHINT
      4 PUSHINT
      24 PUSHINT
      NEWC
      6 STU
      3 STU
      s2 PUSH
      STSLICER
      s0 s5 XCHG2
      STGRAMS
      s1 s4 XCHG
      108 STU
      s1 s2 XCHG
      STREF
      STREF
      ENDC
      3 PUSHINT
      SENDRAWMSG
      NEWC
      s0 s1 s4 XCHG3
      264 PUSHINT
      DICTADDB
      39 THROWIFNOT
      s0 s2 XCHG
    }>c IFREF
    OVER
    2 EQINT
    <{
      264 PUSHINT
      LDSLICEX
      LDGRAMS
      64 LDU
      NEWC
      s0 s4 s6 XCPUXC
      264 PUSHINT
      DICTADDB
      39 THROWIFNOT
      1852798053 PUSHINT
      ZERO
      4 PUSHINT
      24 PUSHINT
      NEWC
      6 STU
      3 STU
      s0 s6 XCHG2
      STSLICER
      s0 s4 XCHG2
      STGRAMS
      s1 s4 XCHG
      107 STU
      s1 s2 XCHG
      32 STU
      64 STU
      ENDC
      3 PUSHINT
      SENDRAWMSG
      s0 s2 XCHG
    }>c IFREF
    SWAP
    3 EQINT
    <{
      DROP
    }> PUSHCONT
    <{
      264 PUSHINT
      LDSLICEX
      LDGRAMS
      64 LDU
      DROP
      s2 s3 PUXC
      264 PUSHINT
      DICTDEL
      39 THROWIFNOT
      1685288050 PUSHINT
      ZERO
      4 PUSHINT
      24 PUSHINT
      NEWC
      6 STU
      3 STU
      s0 s5 XCHG2
      STSLICER
      s0 s3 XCHG2
      STGRAMS
      s1 s3 XCHG
      107 STU
      32 STU
      s1 s2 XCHG
      64 STU
      ENDC
      3 PUSHINT
      SENDRAWMSG
    }>c IFREFELSE
    s0 s3 XCHG
    INC
    NEWC
    32 STU
    s1 s2 XCHG
    32 STU
    256 STU
    STDICT
    ENDC
    POPROOT
  }>
  recv_internal PROC:<{
    SWAP
    CTOS
    4 LDU
    OVER
    ONE
    AND
    <{
      4 BLKDROP
    }> PUSHCONT
    IFJMP
    s2 PUSH
    SBITS
    32 LESSINT
    <{
      4 BLKDROP
    }> PUSHCONT
    IFJMP
    s0 s2 XCHG
    32 LDU
    OVER
    1886156135 PUSHINT
    NEQ
    s2 PUSH
    1685288050 PUSHINT
    NEQ
    AND
    <{
      5 BLKDROP
    }> PUSHCONT
    IFJMP
    s0 s3 XCHG
    LDMSGADDR
    DROP
    DUP
    REWRITESTDADDR
    SWAP
    NEWC
    8 STI
    256 STU
    ENDC
    CTOS
    PUSHROOT
    CTOS
    320 PUSHINT
    SDSKIPFIRST
    LDDICT
    DROP
    DUP2
    264 PUSHINT
    DICTGET
    NULLSWAPIFNOT
    NIP
    NOT
    <{
      7 BLKDROP
    }> PUSHCONT
    IFJMP
    s0 s5 XCHG
    64 LDU
    NEWC
    s5 PUSH
    1886156135 PUSHINT
    EQUAL
    <{
      s8 POP
      DROP
    }> PUSHCONT
    <{
      SWAP
      LDGRAMS
      LDDICT
      DROP
      BALANCE
      UNPAIR
      DROP
      s0 s10 XCHG2
      SUB
      OVER
      GEQ
      80 THROWIFNOT
      1886156135 PUSHINT
      31 PUSHPOW2
      OR
      ZERO
      24 PUSHINT
      s0 s4 XCHG2
      6 STU
      s6 PUSH
      STSLICER
      ROT
      STGRAMS
      s1 s9 XCHG
      STDICT
      106 STU
      s1 s7 XCHG
      32 STU
      s6 s(-1) PUXC
      64 STU
      DUP
      ENDC
      64 PUSHINT
      SENDRAWMSG
      s0 s6 XCHG
    }>c IFREFELSE
    s0 s3 XCHG
    1685288050 PUSHINT
    EQUAL
    <{
      6 BLKDROP
    }> PUSHCONT
    <{
      s0 s4 XCHG2
      264 PUSHINT
      DICTDEL
      DROP
      PUSHROOT
      CTOS
      320 PUSHINT
      SDCUTFIRST
      NEWC
      SWAP
      STSLICER
      STDICT
      ENDC
      POPROOT
      SWAP
      TWO
      AND
      <{
        1685288050 PUSHINT
        31 PUSHPOW2
        OR
        ZERO
        24 PUSHINT
        s0 s5 XCHG2
        6 STU
        s0 s3 XCHG2
        STSLICER
        s3 PUSH
        STGRAMS
        s1 s3 XCHG
        107 STU
        32 STU
        64 STU
        ENDC
        64 PUSHINT
        SENDRAWMSG
      }> PUSHCONT
      <{
        3 BLKDROP
      }> PUSHCONT
      IFELSE
    }>c IFREFELSE
  }>
  is_plugin_installed PROC:<{
    PUSHROOT
    CTOS
    320 PUSHINT
    SDSKIPFIRST
    LDDICT
    DROP
    s0 s2 XCHG
    NEWC
    8 STI
    256 STU
    ENDC
    CTOS
    SWAP
    264 PUSHINT
    DICTGET
    NULLSWAPIFNOT
    NIP
  }>
  get_public_key PROC:<{
    PUSHROOT
    CTOS
    64 PUSHINT
    SDSKIPFIRST
    256 PLDU
  }>
  get_subwallet_id PROC:<{
    PUSHROOT
    CTOS
    32 PUSHINT
    SDSKIPFIRST
    32 PLDU
  }>
  seqno PROC:<{
    PUSHROOT
    CTOS
    32 PLDU
  }>
  get_plugin_list PROC:<{
    NULL
    PUSHROOT
    CTOS
    320 PUSHINT
    SDSKIPFIRST
    LDDICT
    DROP
    <{
      264 PUSHINT
      DICTREMMIN
      NULLSWAPIFNOT2
      s2 POP
      OVER
      <{
        8 LDI
        256 LDU
        DROP
        PAIR
        s0 s3 XCHG2
        PAIR
        s0 s2 XCHG
      }> PUSHCONT
      <{
        DROP
      }> PUSHCONT
      IFELSE
      NOT
    }> PUSHCONT
    UNTIL
    DROP
  }>
}END>c