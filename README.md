#GOCTF
Teaser Levels

Curious to see what types of challenges we have prepared for you? We're happy to release a variety of exploitation, reverse engineering, and crypto challenges.

Don't worry if these seem a little difficult for you - there will be challenges suitable for a variety of skill levels when the event runs.

First up, there's Pumpkin Cake:

    Have you ever written a Power-full exploit before? Here's your chance to do that with a PowerPC remote code execution vulnerability!

Download the binary here

Next up, we have Tie Dye Socks, which has a variety of challenges. Starting off - source code analysis / source reverse engineering:

    Can you analyze the source and request the "FLAG PLEASE\0" ?
    Can you perform some memory reading to disclose the flag at 0xabad1dea?
    Exploit the process and get a shell?
    Perform a format string attack on a 64bit binary?

Following on, there's Tie Dye FTPD, with various challenges including:

    We've heard that there is a backdoor/authentication bypass in the Tie Dye FTPD - can you find it and download the "token"?
    Can you exploit the Tie Dye FTPD process?
    And in 64 bit mode?

Also, there is Eastern Digital, a reverse engineering challenge which features PBKDF and AES-128-CBC.

Don't miss out on reverse engineering "Time To Go". The binary was compiled with GOROOT=/opt/go1.6 GOOS=linux GOARCH=arm GOARM=6 /opt/go1.6/bin/go build -ldflags="-s"

Can you Jump Outdated Elephants? Give it a shot with this binary.

Can you show off your forensics skills with Bona Fortuna? There's a flag in stream 443 and another in 1194.

There's plenty of /heap/ fun to be found in "Remote Pwnage Call", available here

struct d {
  int idx;
  opaque data;
};

struct e {
  int idx;
  int size;
};

/* bringing your RPC into the SUN */
program TOKENPROG {
  version TOKENVERS {
    string GETTOKEN()            = 1; /* get the token for this level */
    int ALLOCATE(int sz)         = 2; /* allocate sz bytes of memory, return the index into the list */
    void FREE(int idx)           = 3; /* free list[idx] if not null */
    void COPY(struct d)          = 5; /* copy bytes into list[idx] */
    struct d INFOLEAK(struct e)  = 7; /* cause an info leak? :P */
  } = 1;
} = 0x20001337;

Looking for more exploitation fun? Do you like playing with Sand Blocks, or performing jail break-in's (which has two flags to be discovered).

Want to break some crypto? Try your hands at Jekyll, or Need Feedback
