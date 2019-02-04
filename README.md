# -*- coding: utf-8 -*-

from linepy import *
from akad.ttypes import *
from multiprocessing import Pool, Process
from akad.ttypes import ContentType as Type
from datetime import datetime
import time,random,sys,json,codecs,threading,glob,re,os,subprocess
from bs4 import BeautifulSoup
from humanfriendly import format_timespan, format_size, format_number, format_length
import time, random, sys, json, codecs, threading, glob, re, string, os, requests, subprocess, six, ast, pytz, urllib, urllib.parse,youtube_dl,pafy,timeit,atexit,traceback
from gtts import gTTS
from googletrans import Translator
#===================================================================================================
# Ini Untuk Login Via Lik Dan Via Emal
#gye = LINE()
#gye = LINE("Email","Password")
#gye.log("Auth Token : " + str(gye.authToken))
#channelToken = gye.getChannelResult()
#gye.log("Channel Token : " + str(channelToken))

# Silahkan Edit Sesukamu
# Asalkan Rapih Dan Respon
# jika ingin login Via qr Ganti Saja
# Atau Login Via Emal
# Mudeng Orang kalo Ra Mudeng
# Sungguh Terlalu
# Jangan Lupa Add Admin 
# id Line ( aisyagye )
#==============================================================================#
botStart = time.time()
#kalo mau login code qr disini pake
gye = LINE()
gye.log("Auth Token : " + str(gye.authToken))
channelToken = gye.getChannelResult()
gye.log("Channel Token : " + str(channelToken))

ais = LINE()
ais.log("Auth Token : " + str(ais.authToken))
channelToken = ais.getChannelResult()
ais.log("Channel Token : " + str(channelToken))

ki2 = LINE()
ki2.log("Auth Token : " + str(ki2.authToken))
channelToken = ki2.getChannelResult()
ki2.log("Channel Token : " + str(channelToken))

ki3 = LINE()
ki3.log("Auth Token : " + str(ki3.authToken))
channelToken = ki3.getChannelResult()
ki3.log("Channel Token : " + str(channelToken))

ki4 = LINE()
ki4.log("Auth Token : " + str(gye.authToken))
channelToken = ki4.getChannelResult()
ki4.log("Channel Token : " + str(channelToken))

ki5 = LINE()
ki5.log("Auth Token : " + str(gye.authToken))
channelToken = ki5.getChannelResult()
ki5.log("Channel Token : " + str(channelToken))

ki6 = LINE()
ki6.log("Auth Token : " + str(gye.authToken))
channelToken = ki6.getChannelResult()
ki6.log("Channel Token : " + str(channelToken))

ki7 = LINE()
ki7.log("Auth Token : " + str(gye.authToken))
channelToken = ki7.getChannelResult()
ki7.log("Channel Token : " + str(channelToken))

ki8 = LINE()
ki8.log("Auth Token : " + str(gye.authToken))
channelToken = ki8.getChannelResult()
ki8.log("Channel Token : " + str(channelToken))

ki9 = LINE()
ki9.log("Auth Token : " + str(gye.authToken))
channelToken = ki9.getChannelResult()
ki9.log("Channel Token : " + str(channelToken))

ki10 = LINE()
ki10.log("Auth Token : " + str(gye.authToken))
channelToken = ki10.getChannelResult()
ki10.log("Channel Token : " + str(channelToken))

ki11 = LINE()
ki11.log("Auth Token : " + str(gye.authToken))
channelToken = ki11.getChannelResult()
ki11.log("Channel Token : " + str(channelToken))

ki12 = LINE()
ki12.log("Auth Token : " + str(gye.authToken))
channelToken = ki12.getChannelResult()
ki12.log("Channel Token : " + str(channelToken))

#kalo mau login menggunakan token
#gunakan disini hapus tanda pagarnya 
#yg atas dinpagar atau bisa juga token di atas 
#di dalam tanda LINE ("TOKEN MU ")
#gye = LINE("Et6qM8UeTce5bGsZG4te.ee6vQU/1ppqr93nt9QLUZG.b5fsCbuxW7zZRtrK5U/74k/53Abd5dWPxfdtLy9bL9I=")
#ais = LINE("Etska0dbjsHvPgZKwmj9.EikS5M3O+L4fOqxjjVgLsq.KlWfvmGVaXdM0yvKM8WGKARpcbAbiKVF9yORPt8QBJw=")
#ki2 = LINE("EtQsqzdJMWn73m72Gup0.OdjJmVnqXLeaZxpJzxDMOa.Z+6ApCht+0H1NeyX50QMD0Yq8oIhYyJ14Yg2yoM/tfc=")
#ki3 = LINE("EtDOOeYj4Rvl5PVfOEaa.ETpCu8czFapUIJQDqIA82G.tcOaI+VmHhWwMbyDL/7yXupWfdIvUJh80yWzu/UJXp8=")
#ki4 = LINE("EtWyu42OHWKSaxPHY3yd.jTri3xzV4E2Z1xvWxjTrRq.s1oy5gbYMT2haZV7l6yzV0bp5gONcnu+bGSSJ1mbT0c=")

KAC = [gye,ais,ki2,ki3,ki4,ki5,ki6,ki7,ki8,ki9,ki10,ki11,ki12]
GUE = [ais,ki2,ki3,ki4,ki5,ki6,ki7,ki8,ki9,ki10,ki11,ki12] # ini jangan luh hapus peak ini fungsi Ciak alias kick
#maksudnya agar bot sb/induk gak ikutan nge kick Mudeng ora
gyeMID = gye.profile.mid
aisMID = ais.profile.mid
ki2MID = ki2.profile.mid
ki3MID = ki3.profile.mid
ki4MID = ki4.profile.mid
ki5MID = ki5.profile.mid
ki6MID = ki6.profile.mid
ki7MID = ki7.profile.mid
ki8MID = ki8.profile.mid
ki9MID = ki9.profile.mid
ki10MID = ki10.profile.mid
ki11MID = ki11.profile.mid
ki12MID = ki12.profile.mid
Bots = [gyeMID,aisMID,ki2MID,ki3MID,ki4MID,ki5MID,ki6MID,ki7MID,ki8MID,ki9MID,ki10MID,ki11MID,ki12MID] #ini jangan dinrubah Gunanya agar bot tidak saling kick
creator = ["u4862fe4b182b2fd194a3108e2f3662e8"]
Owner = ["u4862fe4b182b2fd194a3108e2f3662e8"]
admin = ["u4862fe4b182b2fd194a3108e2f3662e8"]

gyeProfile = gye.getProfile()
aisProfile = ais.getProfile()
ki2Profile = ki2.getProfile()
ki2Profile = ki3.getProfile()
ki2Profile = ki4.getProfile()
ki2Profile = ki5.getProfile()
ki2Profile = ki6.getProfile()
ki2Profile = ki7.getProfile()
ki2Profile = ki8.getProfile()
ki2Profile = ki9.getProfile()
ki2Profile = ki10.getProfile()
ki2Profile = ki11.getProfile()
ki2Profile = ki12.getProfile()

lineSettings = gye.getSettings()
aisSettings = ais.getSettings()
ki2Settings = ki2.getSettings()
ki3Settings = ki3.getSettings()
ki4Settings = ki4.getSettings()
ki5Settings = ki5.getSettings()
ki6Settings = ki6.getSettings()
ki7Settings = ki7.getSettings()
ki8Settings = ki8.getSettings()
ki9Settings = ki9.getSettings()
ki10Settings = ki10.getSettings()
ki11Settings = ki11.getSettings()
ki12Settings = ki12.getSettings()

oepoll = OEPoll(gye)
oepoll1 = OEPoll(ais)
oepoll2 = OEPoll(ki2)
oepoll3 = OEPoll(ki3)
oepoll4 = OEPoll(ki4)
oepoll5 = OEPoll(ki5)
oepoll6 = OEPoll(ki6)
oepoll7 = OEPoll(ki7)
oepoll8 = OEPoll(ki8)
oepoll9 = OEPoll(ki9)
oepoll10 = OEPoll(ki10)
oepoll11 = OEPoll(ki11)
oepoll12 = OEPoll(ki12)

responsename = gye.getProfile().displayName
responsename2 = ais.getProfile().displayName
responsename3 = ki2.getProfile().displayName
responsename2 = ki3.getProfile().displayName
responsename3 = ki4.getProfile().displayName
responsename2 = ki5.getProfile().displayName
responsename3 = ki6.getProfile().displayName
responsename3 = ki7.getProfile().displayName
responsename3 = ki8.getProfile().displayName
responsename3 = ki9.getProfile().displayName
responsename3 = ki10.getProfile().displayName
responsename3 = ki11.getProfile().displayName
responsename3 = ki12.getProfile().displayName
#==============================================================================#



with open('Owner.json', 'r') as fp:
    Owner = json.load(fp)
    
with open('admin.json', 'r') as fp:
    admin = json.load(fp)
    
myProfile = {
	"displayName": "",
	"statusMessage": "",
	"pictureStatus": ""
}

myProfile["displayName"] = gyeProfile.displayName
myProfile["statusMessage"] = gyeProfile.statusMessage
myProfile["pictureStatus"] = gyeProfile.pictureStatus

readOpen = codecs.open("read.json","r","utf-8")
settingsOpen = codecs.open("temp.json","r","utf-8")

#==============================================================================#

read = json.load(readOpen)
settings = json.load(settingsOpen)

def restartBot():
    print ("[ INFO ] BOT RESETTED")
    backupData()
    python = sys.executable
    os.execl(python, python, *sys.argv)
    
def logError(text):
    gye.log("[ ERROR ] " + str(text))
    time_ = datetime.now()
    with open("errorLog.txt","a") as error:
        error.write("\n[%s] %s" % (str(time), text))
        
def sendMessageWithMention(to, mid):
    try:
        aa = '{"S":"0","E":"3","M":'+json.dumps(mid)+'}'
        text_ = '@x '
        gye.sendMessage(to, text_, contentMetadata={'MENTION':'{"MENTIONEES":['+aa+']}'}, contentType=0)
    except Exception as error:
        logError(error)
        
def helpmessage():
    helpMessage = "        🇹🇭⍣ᎢᎬᎪᎷᏴᎾᎢ⅌ᎷᎫ⍣🇹🇭" + "\n" + \
                  "╭════════╬♥" + "\n" + \
                  "║͜͡☆➣ คำสั่ง1 " + "\n" + \
                  "║͜͡☆➣ คำสั่ง2 " + "\n" + \
                  "║͜͡☆➣ คำสั่ง3 " + "\n" + \
                  "╰════════╬♥" + "\n" + \
                  "╭════════╬♥" + "\n" + \
                  "║͜͡☆➣ แทค (แทคทั้งห้อง)" + "\n" + \
                  "║͜͡☆➣ คิกมา ( สั่งบอทเข้าห้อง ) " + "\n" + \
                  "║͜͡☆➣ คิกออก (สั่งบอทออก) " + "\n" + \
                  "║͜͡☆➣ บาย.(ออกหมดทั้งคนทั้งบอท) " + "\n" + \
                  "║͜͡☆➣ เตะ @ (สั่งบอทเตะออก)" + "\n" + \
                  "║͜͡☆➣ เตะดึก @ (สั่งบอทเตะ)" + "\n" + \
                  "║͜͡☆➣ คท " + "\n" + \
                  "║͜͡☆➣ Sp " + "\n" + \
                  "║͜͡☆➣ เชคค่า " + "\n" + \
                  "║͜͡☆➣ นับ " + "\n" + \
                  "║͜͡☆➣ รีบอท " + "\n" + \
                  "║͜͡☆➣ พูด (ใส่ข้อคาม)" + "\n" + \
                  "║͜͡☆➣ เขียน (ใส่ข้อคาม)" + "\n" + \
                  "║͜͡☆➣ เรา " + "\n" + \
                  "║͜͡☆➣ รายชื่อคนในห้อง " + "\n" + \
                  "║͜͡☆➣ เชคคิก " + "\n" + \
                  "╰════════╬♥" + "\n" + \
                  "╭════════╬♥" + "\n" + \
                  "║͜͡☆➣ 🇹🇭⍣ᎢᎬᎪᎷᏴᎾᎢ⅌ᎷᎫ⍣🇹🇭 " + "\n" + \
                  "╰════════╬♥"
    return helpMessage
 
def helptexttospeech():
    helpTextToSpeech =   "  🇹🇭⍣ᎢᎬᎪᎷᏴᎾᎢ⅌ᎷᎫ⍣🇹🇭 " + "\n" + \
                  "╭════════╬♥" + "\n" + \
                  "║͜͡☆➣ เปิดหมด/ปิดหมด »โหมดป้องกันกลุ่ม" + "\n" + \
                  "║͜͡☆➣ Pt on/off »เปิด/ปิดป้องกันเตะ" + "\n" + \
                  "║͜͡☆➣ Qr on/off »เปิด/ปิดป้องกันลิ้งQr" + "\n" + \
                  "║͜͡☆➣ Iv on/off »เปิด/ปิดป้องกันเชิญ" + "\n" + \
                  "║͜͡☆➣ Cc on/off »เปิด/ปิดป้องกันยกเลิกค้างเชิญ" + "\n" + \
                  "║͜͡☆➣ Add on/off »เปิด/ปิดแอดเพื่อนออโต้" + "\n" + \
                  "║͜͡☆➣ Join on/off »เปิด/ปิดระบบมุดลิ้ง" + "\n" + \
                  "║͜͡☆➣ Leave on/off »เปิด/ปิดออกแชทรวม" + "\n" + \
                  "║͜͡☆➣ Sticker on/off »เปิด/ปิดระบบเช็คสติ๊กเกอร์" + "\n" + \
                  "║͜͡☆➣ Read on/off »เปิด/ปิดระบบอ่านออโต้" + "\n" + \
                  "║͜͡☆➣ Dm on/off »เปิด/ระบบเช็คโฟส์" + "\n" + \
                  "║͜͡☆➣ link on/off" + "\n" + \
                  "╰════════╬♥" + "\n" + \
                  "╭════════╬♥" + "\n" + \
                  "║͜͡☆➣ คนสร้างห้อง" + "\n" + \
                  "║͜͡☆➣ ไอดีห้อง" + "\n" + \
                  "║͜͡☆➣ ชื่อห้อง" + "\n" + \
                  "║͜͡☆➣ รายชื่อห้อง" + "\n" + \
                  "║͜͡☆➣ เชคห้อง" + "\n" + \
                  "║͜͡☆➣ ลิ้ง" + "\n" + \
                  "║͜͡☆➣ เปิดลิ้ง" + "\n" + \
                  "║͜͡☆➣ ปิดลิ้ง" + "\n" + \
                  "║͜͡☆➣ พิมตาม on/off " + "\n" + \
                  "║͜͡☆➣ รายชื่อพิมตาม " + "\n" + \
                  "║͜͡☆➣ เพิ่มพิมตาม" + "\n" + \
                  "║͜͡☆➣ ลบพิมตาม" + "\n" + \
                  "║͜͡☆➣ เปิดอ่าน " + "\n" + \
                  "║͜͡☆➣ ปิดอ่าน " + "\n" + \
                  "║͜͡☆➣ ลบเวลาอ่าน " + "\n" + \
                  "║͜͡☆➣ คนอ่าน" + "\n" + \
                  "╰════════╬♥" + "\n" + \
                  "╭════════╬♥" + "\n" + \
                  "║͜͡☆➣ 🇹🇭⍣ᎢᎬᎪᎷᏴᎾᎢ⅌ᎷᎫ⍣🇹🇭 " + "\n" + \
                  "╰════════╬♥"
    return helpTextToSpeech
 
def helptranslate():
    helpTranslate =    "   🇹🇭⍣ᎢᎬᎪᎷᏴᎾᎢ⅌ᎷᎫ⍣🇹🇭 " + "\n" + \
                  "╭════════╬♥" + "\n" + \
                  "║͜͡☆➣ ดำ(ลงคอนแทคที่จะแบน)" + "\n" + \
                  "║͜͡☆➣ เชคดำ" + "\n" + \
                  "║͜͡☆➣ ล้างดำ" + "\n" + \
                  "║͜͡☆➣ รีบอท" + "\n" + \
                  "║͜͡☆➣ บอท " + "\n" + \
                  "║͜͡☆➣ มี " + "\n" + \
                  "║͜͡☆➣ มิด" + "\n" + \
                  "║͜͡☆➣ มิด @" + "\n" + \
                  "║͜͡☆➣ ชื่อ" + "\n" + \
                  "║͜͡☆➣ ตัส" + "\n" + \
                  "║͜͡☆➣ รูป" + "\n" + \
                  "║͜͡☆➣ รูปวีดีโอ" + "\n" + \
                  "║͜͡☆➣ รูปปก" + "\n" + \
                  "║͜͡☆➣ คท @" + "\n" + \
                  "║͜͡☆➣ มิด @" + "\n" + \
                  "║͜͡☆➣ ชื่อ @「Mention」" + "\n" + \
                  "║͜͡☆➣ ตัส @" + "\n" + \
                  "║͜͡☆➣ รูป @" + "\n" + \
                  "║͜͡☆➣ รูปวีดีโอ @" + "\n" + \
                  "║͜͡☆➣ รูปปก @" + "\n" + \
                  "║͜͡☆➣ คนสร้างห้อง" + "\n" + \
                  "║͜͡☆➣ ไอดีห้อง" + "\n" + \
                  "║͜͡☆➣ ชื่อห้อง" + "\n" + \
                  "║͜͡☆➣ รูปห้อง" + "\n" + \
                  "║͜͡☆➣ ลิ้ง" + "\n" + \
                  "║͜͡☆➣ เปิดลิ้ง" + "\n" + \
                  "║͜͡☆➣ รายชื่อห้อง" + "\n" + \
                  "║͜͡☆➣ ปิดลิ้ง" + "\n" + \
                  "║͜͡☆➣ เชคห้อง" + "\n" + \
                  "║͜͡☆➣ เตะ @" + "\n" + \
                  "╰════════╬♥" + "\n" + \
                  "╭════════╬♥" + "\n" + \
                  "║͜͡☆➣ 🇹🇭⍣ᎢᎬᎪᎷᏴᎾᎢ⅌ᎷᎫ⍣🇹🇭" + "\n" + \
                  "╰════════╬♥"
    return helpTranslate 
#==============================================================================#
def backupData():
    try:
        backup = settings
        f = codecs.open('temp.json','w','utf-8')
        json.dump(backup, f, sort_keys=True, indent=4, ensure_ascii=False)
        backup = read
        f = codecs.open('read.json','w','utf-8')
        json.dump(backup, f, sort_keys=True, indent=4, ensure_ascii=False)
        return True
    except Exception as error:
        logError(error)
        return False
        
def command(text):
    pesan = text.lower()
    if pesan.startswith(settings["keyCommand"]):
        cmd = pesan.replace(settings["keyCommand"],"")
    else:
        cmd = "Undefined command"
    return cmd        


def lineBot(op):
    try:
        if op.type == 0:
            print ("[ 0 ] GYEVHA BOTS SATU")
            return
#-------------------------------------------------------------------------------
        if op.type == 25:
            msg = op.message
            if msg.contentType == 13:
                if settings["wblack"] == True:
                    if msg.contentMetadata["mid"] in settings["commentBlack"]:
                        gye.sendMessage(msg.to,"sudah masuk daftar hitam")
                        settings["wblack"] = False
                    else:
                        settings["commentBlack"][msg.contentMetadata["mid"]] = True
                        settings["wblack"] = False
                        gye.sendMessage(msg.to,"Itu tidak berkomentar")
                elif settings["dblack"] == True:
                    if msg.contentMetadata["mid"] in settings["commentBlack"]:
                        del settings["commentBlack"][msg.contentMetadata["mid"]]
                        gye.sendMessage(msg.to,"Done")
                        settings["dblack"] = False
                    else:
                        settings["dblack"] = False
                        gye.sendMessage(msg.to,"Tidak ada dalam daftar hitam")
#-------------------------------------------------------------------------------
                elif settings["wblacklist"] == True:
                    if msg.contentMetadata["mid"] in settings["blacklist"]:
                        gye.sendMessage(msg.to,"sudah masuk daftar hitam")
                        settings["wblacklist"] = False
                    else:
                        settings["blacklist"][msg.contentMetadata["mid"]] = True
                        settings["wblacklist"] = False
                        gye.sendMessage(msg.to,"Done")
                        
                elif settings["dblacklist"] == True:
                    if msg.contentMetadata["mid"] in settings["blacklist"]:
                        del settings["blacklist"][msg.contentMetadata["mid"]]
                        gye.sendMessage(msg.to,"Done")
                        settings["dblacklist"] = False
                    else:
                        settings["dblacklist"] = False
                        gye.sendMessage(msg.to,"Done")
                        
                       
#-------------------------------------------------------------------------------
        if op.type == 25:
            print ("[ 25 ] GYEVHA BOTS TIGA")
            msg = op.message
            text = msg.text
            msg_id = msg.id
            receiver = msg.to
            sender = msg._from
            if msg.toType == 0:
                if sender != gye.profile.mid:
                    to = sender
                else:
                    to = receiver
            else:
                to = receiver
            if msg.contentType == 0:
                if text is None:
                    return
#==============================================================================#
                if text.lower() == 'คำสั่ง1':
                    helpMessage = helpmessage()
                    gye.sendMessage(to, str(helpMessage))
                    gye.sendContact(to,)
                    gye.sendMessage(to,)
                elif text.lower() == 'คำสั่ง2':
                    helpTextToSpeech = helptexttospeech()
                    gye.sendMessage(to, str(helpTextToSpeech))
                    gye.sendMessage(to,)
                elif text.lower() == 'คำสั่ง3':
                    helpTranslate = helptranslate()
                    gye.sendMessage(to, str(helpTranslate))
                    gye.sendMessage(to,)
#==============================================================================#
