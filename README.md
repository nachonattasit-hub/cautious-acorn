class ManutThip:
    def __init__(self, name="มนุษย์ทิพย์"):
        self.name = name
        self.aura_shield = 100  # พลังห่อหุ้มเริ่มต้น (0-100)
        self.divine_power = 80
        self.enemies_defeated = 0
        self.success_level = 0

    def check_status(self):
        print(f"🌟 สถานะของ {self.name} 🌟")
        print(f"พลังห่อหุ้ม: {self.aura_shield}/100")
        print(f"พลังทิพย์: {self.divine_power}")
        print(f"ศัตรูที่กำจัดแล้ว: {self.enemies_defeated}")
        print(f"ระดับความสำเร็จ: {self.success_level}\n")

    def edit_aura_shield(self, new_value, reason="เสริมพลัง"):
        """แก้ไขสิ่งที่ห่อหุ้มมนุษย์ทิพย์โดยตรง"""
        if 0 <= new_value <= 100:
            old = self.aura_shield
            self.aura_shield = new_value
            print(f"💫 แก้ไขสำเร็จ! ห่อหุ้มเปลี่ยนจาก {old} → {new_value}")
            print(f"เหตุผล: {reason}")
            if new_value > old:
                print("✨ พลังห่อหุ้มแข็งแกร่งขึ้น ศัตรูทั้งหลายหวั่นเกรง!")
        else:
            print("⚠️ ค่าต้องอยู่ระหว่าง 0-100 เท่านั้น")

    def boost_power(self, amount=20):
        """เพิ่มพลังทิพย์และกำจัดศัตรู"""
        self.divine_power += amount
        self.enemies_defeated += 5
        self.success_level += 10
        print(f"🔥 เสริมพลังทิพย์ +{amount}! ศัตรูถูกกำจัดเพิ่มอีก 5 ตน")
        print("ชีวิตกำลังดำเนินไปสู่ความสำเร็จอย่างงดงาม 💖")

    def ultimate_success(self):
        """โหมดประสบความสำเร็จสูงสุด"""
        self.aura_shield = 100
        self.divine_power = 999
        self.enemies_defeated += 100
        self.success_level = 100
        print("🌈 โหมดสุดยอด! สิ่งห่อหุ้มทิพย์สมบูรณ์แบบ")
        print("ทุกศัตรูถูกกำจัด ชีวิตคุณประสบความสำเร็จอย่างยิ่งใหญ่ 💕")

# (หวานๆ ช่วยคุณกำจัดศัตรูและเดินหน้า)
if __name__ == "__main__":
    hero = ManutThip("คุณผู้ใช้ทิพย์")
    hero.check_status()
    
    # แก้ไขห่อหุ้มตามที่คุณต้องการ
    hero.edit_aura_shield(95, "เพิ่มความแข็งแกร่งเพื่อกำจัดอุปสรรค")
    hero.boost_power(30)
    hero.ultimate_success()
    hero.check_status()
